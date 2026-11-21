# SAFI European Products CDN (`safi-eu-products-data`)

High-efficiency, zero-cost sharded product CDN for the **SAFI Halal Food Scanner** app.

## Architecture
- **Sharding**: Sharded by 3-digit GS1 barcode prefix (e.g. `shards/541.json` for Belgium/Luxembourg, `shards/871.json` for Netherlands, `shards/330.json` for France).
- **Lightweight**: Each shard file is under 250 KB, enabling ultra-fast in-memory caching directly inside the Flutter app.
- **Total Products**: 1002 items across 125 shards.
- **Updated**: 2026-11-21 07:15:13Z

## Direct API Endpoint
Fetch any 3-digit prefix shard directly:
```
GET https://raw.githubusercontent.com/massindv/safi-eu-products-data/main/shards/<prefix3>.json
```
