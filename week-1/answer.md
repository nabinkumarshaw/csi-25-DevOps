# ========================================
# 1. File Creation and Permission Management
# ========================================

###touch myfile.txt                          # Create a file  
###ls -l myfile.txt                          # Check current permissions  
###chmod u=rwx,g=rx,o=r myfile.txt           # Set permissions: Owner (rwx), Group (rx), Others (r)
###chmod 754 myfile.txt                      # Equivalent numeric permissions
###ls -l myfile.txt                          # Verify changes

# ========================================
# 2. Basic Linux Commands for File & Directory Manipulation
# ========================================

###mkdir demoFolder                          # Create a directory
###cd demoFolder                             # Change into the directory
###touch file1.txt file2.txt                 # Create multiple files
###ls                                        # List files
###rm file2.txt                              # Delete file2.txt
###cd ..                                     # Go back to parent directory
###rm -r demoFolder                          # Remove directory recursively

# ========================================
# 3. Directory Navigation and File Movement
# ========================================

mkdir folderA folderB                     # Create two directories
touch folderA/fileA.txt                   # Create file in folderA
ls folderA                                # List contents
mv folderA/fileA.txt folderB/             # Move file to folderB
cd folderB                                # Navigate to folderB
ls                                        # Verify file is moved

# ========================================
# 4. User and Group Management
# ========================================

sudo groupadd devgroup                    # Create a new group
sudo useradd -m -G devgroup devuser       # Create user and add to group
sudo passwd devuser                       # Set password for user
sudo chown devuser:devgroup myfile.txt    # Change file ownership
ls -l myfile.txt                          # Verify ownership
sudo usermod -aG sudo devuser             # Add user to sudo group
sudo userdel -r devuser                   # Delete user and home directory

# ========================================
# 5. More Linux Command Practice
# ========================================

uname -a                                  # Display system info
whoami                                    # Show current user
pwd                                       # Show current working directory
history                                   # Show command history
cat myfile.txt                            # Display content of a file

# ========================================
# 6. Git Basics and Setup
# ========================================

git config --global user.name "Nabin Kumar Shaw"
git config --global user.email "nabinkumarshaw123@gmail.com"
git init                                  # Initialize Git repo
git status                                # Check Git status

# ========================================
# 7. Commit and Push to Remote
# ========================================

echo "# My Project" > README.md           # Create a README file
git add README.md                         # Stage the file
git commit -m "Initial commit"            # Commit changes
git remote add origin https://github.com/username/repo.git
git push -u origin master                 # Push to remote master

# ========================================
# 8. Branching and Merging with Pull Requests
# ========================================

git checkout -b feature-branch            # Create and switch to a new branch
touch feature.txt                         # Create a new feature file
git add feature.txt                       # Stage the file
git commit -m "Added feature"             # Commit the feature
git push origin feature-branch            # Push the new branch to GitHub

# Then create a Pull Request on GitHub and merge to main.

# ========================================
# 9. Undoing Changes and Deleting Files
# ========================================

git reset --soft HEAD~1                   # Undo last commit (keeps changes)
git rm unwanted.txt                       # Remove file from project
git commit -m "Removed unwanted.txt"      # Commit the removal
git push origin master                    # Push changes to remote

# ========================================
# 10. Merge Conflicts
# ========================================

# After editing and resolving conflict manually
git add conflicted-file.txt
git commit -m "Resolved merge conflict"   # Commit the resolution
