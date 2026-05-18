# Use the latest available tag from Docker Hub
ARG BUILD_FROM=bizmodeller/mymediaforalexa:latest
FROM $BUILD_FROM

# HAOS requires this label for add-ons
LABEL io.hass.version="1.3.156" \
      io.hass.type="addon" \
      io.hass.arch="armhf|aarch64|i386|amd64"
