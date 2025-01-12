# Removing-diacritics-on-consonants-linux-

The goal of this repository is to modify the keyboard layout so that the combination of `´` (dead acute) + a consonant results in `’` (typographically correct apostrophe) followed by the consonant (e.g., `’s`, `’w`, `’c`).

In Spanish, diacritics (tildes) are only used on vowels. This project removes accented consonants like `ś`, `ẁ`, and `ć`, replacing them with the intended `’s`, `’w`, and `’c`.

## Instructions:

### 1. Download the `.XCompose` File

To simplify the process, this repository provides a pre-configured `.XCompose` file.

1. Navigate to the `Raw` view of the `.XCompose` file in this repository.
2. Download it and save the `.XCompose` file to your home directory.

My manjaro system automatically detected this file upon restarting and fixed the issue, but below are some additional instructions you may want to follow if it doesn´t fix your issue.

### 2. Set Up Environment Variables

For your system to recognize the `.XCompose` file and its custom sequences, you need to configure the following environment variables:

#### For Xorg:

1. Add the following lines to your shell configuration file (e.g., `~/.bashrc` or `~/.zshrc`):
   ```bash
   export XCOMPOSEFILE=~/.XCompose
   export XMODIFIERS="@im=local" ```
   (I´m not sure about these, I think just the first one should be enough)

2. Apply the changes immediately by running:
   ```bash
   source ~/.bashrc
   ```

3. Restart you computer.




