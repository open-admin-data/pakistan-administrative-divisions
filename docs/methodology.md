# Methodology

## Data Sources

- **OCHA COD-AB Pakistan** (CC BY-IGO) — Province, district, and tehsil records with P-codes and centroid coordinates
- **agriSmartPakistan** — Urdu names for provinces, districts, and tehsils
- **Wikidata** (CC0) — Supplementary Urdu district names
- **RavelloH/iso-3166-2-locale** — Additional Urdu city/tehsil names
- **GeoNames** (CC BY 4.0) — Postal codes matched by proximity (2,563 postal zones)

## Processing

1. Administrative records from OCHA COD-AB XLSX gazetteer
2. Urdu names merged from multiple sources (100% province + district, 57% tehsil)
3. Postal codes matched from GeoNames postal dump by lat/lon proximity (100% coverage)
4. Multi-format export: JSON, NDJSON, CSV

## Accuracy

- Coordinates: 100% at all levels (from OCHA COD-AB centroids)
- Urdu names: 100% province + district, 57% tehsil (remainder uses romanized local names)
- Postal codes: 100% at district and tehsil levels
- Build script is idempotent: same input always produces same output