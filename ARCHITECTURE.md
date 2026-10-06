# Proje Mimarisi

## 1. Temel Yapı
- **Tech Stack:** [Tech stack buraya yazılacak]
- **Mimari Desen:** Feature-First / Clean Architecture

## 2. Veri Akışı ve Kurallar
- Modüller arası bağımlılıklar tek yönlü olmalıdır.
- State yönetimi ve yan etkiler (side-effects) birbirinden ayrılmalıdır.
- Dış bağımlılıklar (API client, Database vb.) arayüzler (Interfaces/Protocols) arkasında soyutlanmalıdır.

## 3. Deployment Stratejisi
- Stateless (Durumsuz) uygulama mimarisi.
- Docker konteynerleri üzerinden bulut bağımsız (AWS, Hetzner vb.) dağıtım.
