# Use the golang base image
FROM golang:1.18-alpine AS build

# Set the Current Working Directory inside the container
WORKDIR /app

# Copy the Go source file
COPY server.go .

# Build the Go app
RUN go build -o server server.go

# Start a new stage from scratch
FROM alpine:latest  

# Create the directory
WORKDIR /app

# Copy the Pre-built binary file from the build stage
COPY --from=build /app/server .

# Expose the service port
EXPOSE 8001

# Command to run the binary
CMD ["./server"]

