# Tone Canvas Project

**Tone Canvas** is a comprehensive, modern web-based tool designed to assist beginners, especially children, in learning tones and intonation across various devices. The project integrates a user-friendly front-end built with Next.js and a robust Flask-based backend, enabling seamless interaction and effective learning experiences.

---

## Project Overview

### Why Tone Canvas?
Tones and intonation often carry critical non-verbal information in language. For instance:
- In non-tonal languages like French and English, variations in intonation can imply different or even opposite meanings.
- In tonal languages like Mandarin and Vietnamese, tonal differences can entirely alter the meaning of a word. For example, in Mandarin:
  - *mā* means "mother,"
  - *má* refers to a fabric,
  - *mǎ* means "horse,"
  - *mà* means "quarrel."

**Tone Canvas** leverages a simple interface, intuitive interactions, and multimodal feedback to help beginners effectively learn and retain these linguistic nuances.

---

## Repository Structure
This project consists of two primary repositories:

1. **Frontend Repository**
   - Built with [Next.js](https://nextjs.org).
   - Provides the user interface for interaction.

2. **Backend Repository**
   - Built with [Flask](https://flask.palletsprojects.com).
   - Handles audio file management, pitch data processing, and user interactions through APIs.

---

## Frontend Overview

### Getting Started
1. Clone the frontend repository:
   ```bash
   git clone https://github.com/your-username/frontend-repo.git
   cd frontend-repo
   ```
2. Run the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```
3. Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

### Key Features
- Optimized font loading with [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts).
- Hot-reloading for seamless development.

### Deployment
Deploy the frontend easily using the [Vercel Platform](https://vercel.com).

---

## Backend Overview

### Project Structure
```
.
├── backend-dev.yaml        # Docker Compose configuration for development
├── Dockerfile              # Dockerfile for containerized deployment
├── flask_app.py            # Main Flask application entry point
├── requirements.txt        # Python dependencies
├── [corpus]                # Directory for storing .wav and .Pitch files
├── [data_base]             # Directory for storing user-generated YAML files
├── [temp]                  # Temporary files directory
└── [utils]                 # Utility scripts for modular functionality
```

### Getting Started
1. Clone the backend repository:
   ```bash
   git clone https://github.com/your-username/backend-repo.git
   cd backend-repo
   ```
2. Install dependencies:
   ```bash
   python -m venv .env
   source .env/bin/activate   # For Linux/macOS
   .env\Scripts\activate    # For Windows
   pip install -r requirements.txt
   ```
3. Run the Flask application:
   ```bash
   python flask_app.py
   ```

### API Endpoints
#### Example:
- **GET /api/get-pitch-json**
  - Returns interpolated pitch data for the current `.wav` file.
  - **Response**:
    - `200`: JSON containing pitch data.
    - `404`: "No wav files found."

For the full list of endpoints, refer to the backend repository's README.

### Deployment with Docker
Build and run the backend in a container:
```bash
docker-compose -f backend-dev.yaml up --build
```

---

## Combined Deployment
To integrate both front-end and back-end repositories into a unified project:

1. **Clone Both Repositories**:
   ```bash
   mkdir tone-canvas-main
   cd tone-canvas-main
   git submodule add https://github.com/your-username/frontend-repo.git frontend
   git submodule add https://github.com/your-username/backend-repo.git backend
   ```

2. **Run Frontend and Backend**:
   - Start the backend Flask server.
   - Start the frontend development server.

3. **Access the Application**:
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend: [http://localhost:5000](http://localhost:5000)

---

## Contribution Guidelines
Contributions are welcome! To contribute:
1. Fork the relevant repository (frontend or backend).
2. Create a feature branch.
3. Submit a pull request with detailed explanations.

---

## License
This project is licensed under the Apache 2.0 License. For details, refer to the LICENSE file in each repository.

---

## Learn More
- [Next.js Documentation](https://nextjs.org/docs) - Learn about Next.js features and APIs.
- [Flask Documentation](https://flask.palletsprojects.com) - Learn about Flask's capabilities.
- [Docker Documentation](https://docs.docker.com) - Learn about containerized deployment.

Happy coding!

