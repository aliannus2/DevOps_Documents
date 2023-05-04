<style>
.code-block {
  background-color: black;
  color: white;
  padding: 10px;
  border-radius: 5px;
  white-space: pre;
  font-family: monospace;
}
</style>

# Lens Desktop Installation on Ubuntu

This guide explains how to install the Lens Kubernetes IDE on Debian-based systems such as Ubuntu.

## Step 1: Add Lens public security key to your keyring

Run the following command to download and add the Lens public security key to your keyring:

<div class="code-block">
curl -fsSL https://downloads.k8slens.dev/keys/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/lens-archive-keyring.gpg > /dev/null
</div>

## Step 2: Add the Lens repository

Add the Lens repository to your /etc/apt/sources.list.d directory with the following command:

<div class="code-block">
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/lens-archive-keyring.gpg] https://downloads.k8slens.dev/apt/debian stable main" | sudo tee /etc/apt/sources.list.d/lens.list > /dev/null
</div>

## Step 3: Install or update Lens Desktop

Update your package lists and install Lens Desktop by running:

<div class="code-block">
sudo apt update
sudo apt install lens
</div>

## Step 4: Run Lens Desktop

Launch Lens Desktop from the command line by typing:

<div class="code-block">
lens-desktop
</div>

Alternatively, you can find Lens Desktop in your system's application launcher.

That's it! You've successfully installed Lens Desktop on your Ubuntu system.
