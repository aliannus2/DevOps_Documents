# Lens Desktop Installation on Ubuntu

This guide explains how to install the Lens Kubernetes IDE on Debian-based systems such as Ubuntu.

## Step 1: Add Lens public security key to your keyring

Run the following command to download and add the Lens public security key to your keyring:

```curl -fsSL https://downloads.k8slens.dev/keys/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/lens-archive-keyring.gpg > /dev/null```

## Step 2: Add the Lens repository

Add the Lens repository to your /etc/apt/sources.list.d directory with the following command:

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/lens-archive-keyring.gpg] https://downloads.k8slens.dev/apt/debian stable main" | sudo tee /etc/apt/sources.list.d/lens.list > /dev/null

## Step 3: Install or update Lens Desktop

Update your package lists and install Lens Desktop by running:

```
sudo apt update
sudo apt install lens
```

## Step 4: Run Lens Desktop

Launch Lens Desktop from the command line by typing:

```lens-desktop```

Alternatively, you can find Lens Desktop in your system's application launcher.

That's it! You've successfully installed Lens Desktop on your Ubuntu system.
