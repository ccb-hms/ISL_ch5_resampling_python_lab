FROM ghcr.io/rocker-org/devcontainer/r-ver:4.5

# Install Python packages during build to avoid PEP 668 issues
# Copy requirements file
COPY requirements.txt /tmp/requirements.txt

# Install packages using pip with --break-system-packages flag
# This is safe in a container environment
RUN pip install --break-system-packages -r /tmp/requirements.txt

# Clean up
RUN rm /tmp/requirements.txt
