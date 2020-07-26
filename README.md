# cli_password_generator
Generate a random password of a specified length

## Installation

Download newpass.py and put it in your PATH (~/bin for instance)  
Recommend renaming to newpass for easier use on the command line  
Make it executable (chmod u+x newpass)

## Usage

usage: newpass [option] [length]

Generate a random password of a specified length

positional arguments:

    length        Desired password length. If not specified, default is 23

optional arguments:

    -h, --help    show this help message and exit
  
    --symbol, -s  Include all symbols in the password
  
    --limit, -l   Limit symbols used to !@#$%&*

examples:

    newpass - generates a 23 character alphanumeric password
    newpass 20 - generates a 20 character alphanumeric password
    newpass -s 25 - generates a 25 character password that can include all symbols
    newpass -l 15 - generates a 15 character password that can include symbols !@#$%&*

    If both -s and -l flags are used (-sl, -ls) the -s takes 
    precedence and the -l is ignored

    Passwords created always start with a letter, contain at least
    one capital and one lowercase letter and at least 3 digits
    
## Notes:

Some sites restrict the use of symbols. 
The default does not include symbols. 

The -s flag includes a larger list of symbols (!"#$%&\'()*+,-:;=?@[\]^_{}~)

The -l flag includes a limited set of symbols (!@#$%*&) for increased acceptance to some sites.


Use a unique password for every site and never reuse passwords.  
Store them in a password manager such as KeePass, LastPass, or [Bitwarden](https://bitwarden.com/)

