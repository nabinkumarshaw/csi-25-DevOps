Linux and Git Practice Assignment

1. File Creation and Permission Management

Commands:

touch myfile.txt                     # Create a file
ls -l myfile.txt                     # Check current permissions
chmod u=rwx,g=rx,o=r myfile.txt      # Set permissions: Owner (rwx), Group (rx), Others (r)
chmod 754 myfile.txt                 # Equivalent using numeric notation
ls -l myfile.txt                     # Verify changes

2. Basic Linux Commands for File & Directory Manipulation

Commands:

mkdir demoFolder                   # Create directory
cd demoFolder                      # Change directory
touch file1.txt file2.txt          # Create files
ls                                 # List files
rm file2.txt                       # Remove file
cd ..                              # Go back one directory
rm -r demoFolder                   # Remove directory recursively

3. Directory Navigation and File Movement

Commands:

mkdir folderA folderB
touch folderA/fileA.txt
ls folderA                         # List files in folderA
mv folderA/fileA.txt folderB/      # Move file from folderA to folderB
cd folderB                         # Navigate to folderB
ls                                 # Verify file is moved

4. User and Group Management

Commands:

sudo groupadd devgroup
sudo useradd -m -G devgroup devuser
sudo passwd devuser
sudo chown devuser:devgroup myfile.txt
ls -l myfile.txt                   # Check ownership
sudo usermod -aG sudo devuser      # Add user to sudo group
sudo userdel -r devuser            # Delete user and home directory

5. More Linux Command Practice

Commands:

uname -a                          # System information
whoami                            # Current user
pwd                               # Current working directory
history                           # Command history
cat file.txt                      # View file content

6. Git Basics and Setup

Commands:

git config --global user.name "Nabin Kumar Shaw"
git config --global user.email "nabinkumarshaw123@gmail.com"
git init                           # Initialize Git repo
git status                         # Check status

7. Commit and Push to Remote

Commands:

echo "# My Project" > README.md
git add README.md
git commit -m "Initial commit"
git remote add origin https://github.com/username/repo.git
git push -u origin master

8. Branching and Merging with Pull Requests

Commands:

git checkout -b feature-branch
touch feature.txt
git add feature.txt
git commit -m "Added feature"
git push origin feature-branch
# Then create a Pull Request on GitHub and merge to main

9. Undoing Changes and Deleting Files

Commands:

git reset --soft HEAD~1                    # Undo last commit (keeps changes)
git rm unwanted.txt                        # Remove file
git commit -m "Removed unwanted.txt"
git push origin master

10. Merge Conflicts

git add conflicted-file.txt
git commit -m "Resolved merge conflict"

