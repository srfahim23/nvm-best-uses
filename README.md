# nvm-best-uses

Step 1: Update Your System:

if debian : Before installing NVM, update your package lists: sudo apt update && sudo apt upgrade -y

Step 2: Install Required Dependencies :Ensure you have curl or wget installed: (if debian: sudo apt install curl -y
)

or : sudo apt install wget -y


Step 3: Download and Install NVM: Run the following command to install NVM: curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

If you prefer wget, use: wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

Step 4: Load NVM in Your Shell: Once the installation is complete, load NVM into your shell session: 

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"


To ensure NVM loads automatically in new terminal sessions, add these lines to your shell configuration file:

    For Bash (~/.bashrc): 

    echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.bashrc
echo '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"' >> ~/.bashrc
echo '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"' >> ~/.bashrc


For Zsh (~/.zshrc):

echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"' >> ~/.zshrc
echo '[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"' >> ~/.zshrc


Then apply the changes: source ~/.bashrc  # or source ~/.zshrc if using Zsh


Step 5: Verify the Installation: Check if NVM is installed correctly: nvm --version


Step 6: Install Node.js Using NVM

You can now install Node.js: nvm install --lts  # Installs the latest LTS version

Or install a specific version: nvm install 18

optional: Set a default Node.js version:
nvm use 18
nvm alias default 18

Check the installed Node.js version: node -v

