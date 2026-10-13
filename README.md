# ZetaFlow

**ZetaFlow** is a blazing-fast, low-latency load balancer written in modern **C++23**, built for high-performance systems and microservice orchestration. It supports **dual protocols** – both **HTTP** and **gRPC** – and provides multiple customizable load balancing strategies.

---

## 🚀 Features

- ⚡ **High Performance**: Optimized for low latency with Boost.Asio and modern C++23.
- 🌐 **Dual Protocol Support**: Seamless handling of both HTTP and gRPC traffic.
- ♻️ **Pluggable Load Balancing Strategies**:
  - Round Robin
  - Least Connections
  - Consistent Hashing
  - Random Selection
- 👷️ **Modular Design** using Software Design Patterns: Strategy, Factory, Observer, and Proxy.
- 📦 **Robust Build System**:
  - **CMake** for build configuration
  - **Conan** for package and dependency management

---

## 🧱 Tech Stack

- **Language**: C++23
- **Networking**: [Boost.Asio](https://www.boost.org/doc/libs/release/doc/html/boost_asio.html)
- **Protocols**: HTTP, gRPC (via [gRPC C++](https://grpc.io/docs/languages/cpp/))
- **Serialization**: Protocol Buffers
- **Build System**: CMake
- **Package Manager**: Conan

---

## 📁 Project Structure

```
zetaflow
├── src
├── include
├── proto
├── generated
├── build
├── CMakeLists.txt
├── conanfile.txt
├── README.md
└── LICENSE
```

---

## 🛠️ Build Instructions

### 1. Install Dependencies

Ensure you have:
- CMake (>= 3.20)
- Conan (>= 2.0)
- g++ with C++23 support
- Protobuf compiler (`protoc`)
- gRPC C++ libraries

### 2. Clone and Build

```bash
git clone https://github.com/yourusername/zetaflow.git
cd zetaflow
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build .
```

### 3. Run

```bash
./zetaflow
```

---

## 🧪 Load Balancing Strategies

You can select the strategy via a config file or CLI flags:

| Strategy             | Description                              |
|----------------------|------------------------------------------|
| `round_robin`        | Cycles through backends sequentially     |
| `least_connections`  | Picks backend with fewest active conns   |
| `consistent_hashing`| Maps requests to consistent backends     |
| `random`             | Chooses a backend at random              |

---

## 📚 Documentation

- Full API docs coming soon.
- For now, refer to `include/` and `src/strategy/` for extensibility.

---

## 🌐 Acknowledgments

- [Boost C++ Libraries](https://www.boost.org/)
- [gRPC C++](https://grpc.io/)
- [Conan Package Manager](https://conan.io/)

