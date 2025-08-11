# api-docs
Official API documentation and quickstart 
```markdown
# ContentVeritas API Documentation

Official documentation and examples for the ContentVeritas AI Content Authentication API.

## Quick Start

1. Get your API key at [contentveritas.com](https://contentveritas.com)
2. Make your first request:

```bash
curl -X POST https://contentveritas.com/api/v1/validate \
```json
{
  "consensus_score": 0.75,
  "confidence": 0.92,
  "individual_scores": {
    "detector_1": 0.73,
    "detector_2": 0.77,
    "detector_3": 0.74
  },
  "processing_time": 0.234,
  "status": "success"
}
  -H "Content-Type: application/json" \
  -H "X-API-Key: YOUR_API_KEY" \
  -d '{
    "text": "Content to analyze",
    "options": {
      "category": "general",
      "return_details": true
    }
  }'
```

## Response Format

```json
{
  "consensus_score": 0.85,
  "confidence": 0.92,
  "processing_time": 0.234,
  "classification": "likely_ai",
  "individual_scores": {
    "detector_1": 0.87,
    "detector_2": 0.83,
    "detector_3": 0.86
  }
}
```

## Authentication

All API requests require authentication using your API key in the header:
`X-API-Key: YOUR_API_KEY`

## Rate Limits

- **Basic**: 1,000 requests/hour
- **Pro**: 10,000 requests/hour
- **Enterprise**: 100,000 requests/hour

## Support

- Email: api-support@contentveritas.com
- Documentation: [docs.contentveritas.com](https://docs.contentveritas.com)

```
