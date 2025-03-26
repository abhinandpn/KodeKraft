<<<<<<< HEAD
```markdown
# KodeKraft

KodeKraft is a large-scale, microservices-based educational platform enabling users to buy and sell courses, manage online classes, and provide institution-level support. It supports advanced features like AI chat assistance, gRPC-based microservices, and real-time communication using Kafka and RabbitMQ.

## 🚀 Project Overview

KodeKraft is designed to deliver an advanced educational platform with features such as:

- **User Management**: Students, instructors, and institutions.
- **Course Management**: Course creation, purchase, and subscription models.
- **Payment Integration**: Supports Razorpay payments and recharge coupons.
- **AI Assistance**: AI-driven chatbot for learning support.
- **Community Features**: Discord-like forums for user interaction.
- **Scalability**: Built with Docker, Kubernetes, and gRPC for microservices.
- **Caching**: Implements Redis for caching and performance optimization.

## 📁 Project Structure

```
KodeKraft/
├── user-service/          # User Management Microservice
│   ├── proto/             # gRPC Definitions
│   ├── service/           # Business Logic
│   └── main.go            # gRPC Server Entry Point
│
├── course-service/        # Course Management Microservice
│
├── payment-service/       # Payment & Coupon Microservice
│
├── common/                # Shared Code (gRPC stubs, utilities)
│   └── pb/                # Generated gRPC Code
│
├── redis/                 # Redis Cache Integration
│
└── README.md              # Project Documentation
```

## 🛠️ Tech Stack

- **Language**: Go (Golang)
- **Communication**: gRPC (for microservices communication)
- **Caching**: Redis (performance optimization)
- **Databases**:
  - PostgreSQL (User and Payment data)
  - MongoDB (Course content and metadata)
  - Cassandra (Analytics and reporting)
  - SpannerDB (Scalable institutional data)
- **Event Streaming**: Kafka (for real-time communication)
- **Task Queue**: RabbitMQ (for asynchronous tasks)
- **Deployment**: Docker & Kubernetes (container orchestration)

## 📌 Setup Instructions

### Prerequisites

- Go (>= 1.22)
- Docker & Docker Compose
- Protocol Buffers Compiler

### Clone the Repository

```bash
git clone https://github.com/abhinandpn/KodeKraft.git
cd KodeKraft
```

### Install Dependencies

```bash
# For gRPC
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```

### Generate gRPC Code

```bash
protoc --go_out=./common/pb --go-grpc_out=./common/pb user-service/proto/user.proto
```

### Run Services

1. Start Redis:

```bash
docker-compose up -d redis
```

2. Start the User Service:

```bash
cd user-service
go run main.go
```

## 📊 Microservices

1. **User Service**
    - gRPC Methods: CreateUser, GetUser
    - Database: PostgreSQL
    - Caching: Redis (User Session Management)

2. **Course Service**
    - gRPC Methods: CreateCourse, GetCourse, ListCourses
    - Database: MongoDB

3. **Payment Service**
    - gRPC Methods: CreateTransaction, VerifyPayment
    - Database: PostgreSQL

## 📚 API Usage

### Create a User

```bash
grpcurl -plaintext -d '{"name": "John Doe", "email": "john@example.com", "password": "password", "role": "student"}' localhost:50051 user.UserService/CreateUser
```

## 🧪 Testing

Run unit tests for all services:

```bash
go test ./...
```

## 📄 License

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## 📣 Contributing

Contributions are welcome! Feel free to open issues and submit pull requests.

## 📞 Contact

For support, contact [yourname@example.com](mailto:yourname@example.com).
```
=======
# KodeKraft
>>>>>>> 685fd0f (Initial commit with README)
