# 🧩 System Architecture – Planner 5D DIY (AI-Assisted Interior Design)

## Overview

Planner 5D DIY is a simplified, AI-powered home and interior design platform tailored for non-professionals.  
It provides an intuitive interface that allows users to visualize, redesign, and personalize their spaces using natural language prompts or drag-and-drop tools.

This document outlines the technical foundation of the product — its frontend, backend, database, integrations, and communication flow.

---

## 🏗️ Architecture Summary

The system is built on a **modular, cloud-based architecture** designed for scalability, speed, and ease of integration with AI models and third-party services.

**Architecture Layers:**
1. **Frontend (Client Application)** – User interface and experience layer.
2. **Backend (API Layer)** – Core business logic, AI orchestration, and data processing.
3. **Database Layer** – Storage for user data, projects, and design assets.
4. **AI Services** – Image generation, design recommendation, and style analysis.
5. **Third-Party Integrations** – Authentication, payment, and file-storage systems.

---

## 🎨 Frontend Architecture

### Tech Stack
- **Framework:** React + Vite  
- **UI Library:** Tailwind CSS + Framer Motion  
- **State Management:** Redux Toolkit  
- **3D Rendering:** Three.js / Babylon.js  
- **AI Prompt UI:** Custom React components for image upload + text prompts  
- **Hosting:** Vercel / Netlify  

### Functionality
- User authentication and profile management  
- AI prompt interface for room redesign  
- Drag-and-drop layout editor (with furniture and décor assets)  
- Real-time preview of 3D spaces  
- Export and share options (image / web link)

---

## ⚙️ Backend Architecture

### Tech Stack
- **Framework:** Node.js + Express  
- **AI Middleware:** Python Flask microservice / FastAPI (for AI inference)  
- **Authentication:** JWT-based Auth / OAuth 2.0 (Google & Apple)  
- **Storage:** AWS S3 / Firebase Storage (for images and models)  
- **APIs:** REST / GraphQL  

### Core Services
- **AI Redesign Service:** Handles user image uploads and communicates with AI models (OpenAI / Replicate / Stability AI)  
- **Project Management Service:** Saves user projects, room configurations, and preferences  
- **Rendering Service:** Generates 2D & 3D views via Three.js pipeline  
- **Notification Service:** Email / in-app alerts for saved or shared projects  

---

## 🗄️ Database Layer

### Database Choices
- **Primary DB:** PostgreSQL (for structured user and project data)  
- **Secondary DB:** MongoDB (for AI logs and unstructured data)  
- **Cache:** Redis (for session management and fast fetches)  

### Data Entities
- **Users:** Authentication data, profiles, preferences  
- **Projects:** Room layouts, AI render outputs, saved states  
- **Assets:** Furniture, textures, and color palettes  
- **Prompts:** User inputs and AI responses for history tracking  

---

## 🤖 AI Integration Layer

### Components
- **Image to Style Model:** Translates user photos into editable 3D spaces  
- **Text-to-Design Model:** Uses prompts to generate styled interiors (e.g., “Make this room Scandinavian-style”)  
- **Style Matching Engine:** Analyzes user-provided reference images and suggests decor themes  
- **Feedback Loop:** Users can refine AI outputs via iterative prompt adjustments  

### Model Hosting
- AI models hosted via Hugging Face / Replicate / custom cloud GPU servers  

---
