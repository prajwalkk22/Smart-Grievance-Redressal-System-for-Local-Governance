# Architecture (v0.1)

1. Citizen submits complaint (image/text/voice) from frontend.
2. API Gateway routes it to `complaint-service`.
3. Complaint goes into MongoDB, and image/text/audio pushed to `ai-service` via RabbitMQ.
4. `ai-service` classifies it, updates category in DB.
5. Admin views complaint via `admin-portal`.
6. Admin updates status → Notification sent via `notification-service`.
7. Citizens can track status live.
