# 🖥️ Windows 7 in Docker Container #
Docker KVM Windows

A Docker container solution for running Windows 7 with KVM acceleration, providing remote access via VNC and RDP.

# 🚀 Getting Started #
Prerequisites
Docker installed
KVM enabled system
Administrative privileges
# 📦 Features #
⚡ Run Windows 7 inside a Docker container
🔒 Secure with isolated environment
🖥️ Access via noVNC (web browser) or RDP
🚀 Fast virtualization using KVM (requires host support)
💾 Persistent storage using Docker volumes
# 🛠️ Requirements #
Linux host with:
KVM enabled (/dev/kvm should exist)
Docker installed
Windows 10 ISO (for initial installation)
Modern web browser (for noVNC access)
# 🚀 Installation #

git clone https://github.com/PixelPlayz69/win7vm

cd win7vm

docker build -t windows7-vm .

docker run -it --rm \
    --device /dev/kvm \
    -p 6080:6080 \
    -p 3389:3389 \
    -v windows_data:/data \
    -v windows_iso:/iso \
  windows7-vm 
