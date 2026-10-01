# Chinese -> Khmer Video Dubber

Long-form Chinese-to-Khmer video dubbing starter.

Pipeline: upload -> extract/split audio -> Chinese transcription with timestamps -> Khmer translation -> Khmer neural TTS -> timing fit -> final MP4.

## Run locally

1. Copy `.env.example` to `.env` and add OpenAI + Azure Speech credentials.
2. Run `docker compose up --build`.
3. Open http://localhost:3000.

There is no hardcoded video-duration limit in the worker. Real limits are storage, provider quotas/rate limits, processing time, and server resources. For production, use direct multipart uploads to S3/R2/Azure Blob instead of sending multi-GB files through FastAPI.
