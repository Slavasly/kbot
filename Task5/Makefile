IMAGE_NAME=quay.io/slavasly/kbot
VERSION=v1.0.0
TAG=$(IMAGE_NAME):$(VERSION)

.PHONY: image clean

image:
    docker build -t $(TAG) .

clean:
    docker rmi $(TAG) || true

# linux:
# 	docker build -t linux-(TARGETOS=linux)

# arm64:
# 	docker build -t arm64-(TARGETARCH=arm64)

# macOS:
# 	docker build -t macOS-(TARGETOS=darwin)

# windows:
# 	docker build -t windows-(TARGETOS=windows)

# clean:
# 	docker rmi <IMAGE_TAG>
