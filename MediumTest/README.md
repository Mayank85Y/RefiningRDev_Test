# MediumTest - Building R from a Specific Subversion Revision in the R Dev Container

## 🚀 Creating bash script for Building R Subversion

1. **Open the R Dev Container**  
   - Start the Dev Container in **GitHub Codespaces**  
   - Open a **Bash terminal** inside VS Code.

2. **Write Bash Script**
   - Make a Script which take the R Subversion as input and downlaod the required version.
   - Make script executable `chmod +x scriptname.sh`
   - Now Build R from revision 86123 with `./scriptname.sh 86123`

## Test

The following code is Bash Script code required for Building R from a Specific Subversion.

```markdown
```r
#!/bin/bash

# Check for required argument
if [ -z "$1" ]; then
  echo "Usage: $0 <revision-number>"
  exit 1
fi

REVISION=$1

echo "Building R from Subversion revision: $REVISION"

# Install subversion (if not install)
sudo apt-get update && sudo apt-get install -y subversion

# Checkout specified revision
svn checkout -r "$REVISION" https://svn.r-project.org/R/trunk R-devel

# Build R
cd R-devel || { echo "Failed to enter directory"; exit 1; }
./configure --enable-R-shlib
make 
```

Here is the screenshot of R session required for Medium Test

### Script

![alt text](<Screenshot 2025-03-15 185151.png>)

### Shell Running

![alt text](<Screenshot 2025-03-15 185321.png>)

![alt text](<Screenshot 2025-03-15 185353.png>)

![alt text](<Screenshot 2025-03-15 185506.png>)

![alt text](<Screenshot 2025-03-15 185844.png>)

![alt text](<Screenshot 2025-03-15 192206.png>)
