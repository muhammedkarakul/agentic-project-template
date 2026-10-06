# syntax=docker/dockerfile:1

# ---- Base ----
FROM alpine:3.20 AS base
WORKDIR /app
ENV APP_ENV=production

# ---- Dependencies ----
FROM base AS deps
# TODO: Dil/runtime'a göre bağımlılık kurulumunu buraya ekle
#   Node:   COPY package*.json ./ && RUN npm ci
#   Python: COPY requirements.txt ./ && RUN pip install -r requirements.txt
#   Go:     COPY go.mod go.sum ./ && RUN go mod download

# ---- Builder ----
FROM deps AS builder
COPY . .
# TODO: Build adımını buraya ekle (örn. npm run build / go build / vb.)

# ---- Runtime ----
FROM base AS runtime
RUN addgroup -S app && adduser -S app -G app
COPY --from=builder /app /app
USER app
EXPOSE 8080
# TODO: Uygulamayı başlatan komutu buraya ekle
CMD ["sh", "-c", "echo 'Define your start command in docker/Dockerfile' && sleep infinity"]
