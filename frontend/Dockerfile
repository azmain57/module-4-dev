
# ---------- Build Frontend ----------
FROM node:18-alpine AS frontend-build

WORKDIR /frontend
COPY frontend/package*.json ./
RUN npm install
COPY frontend .
RUN npm run build

# Copy frontend build to backend public folder
COPY --from=frontend-build /frontend/dist ./public