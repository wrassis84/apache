1 - Verify and install pip3:
sudo apt update && sudo apt install python3-pip
2 - Since this example will be using Docker as the infrastructure source, the docker-py package is required as well:
pip3 install molecule docker
3 - Install the linters for ansible and yaml:
Note: For more details: https://ansible-lint.readthedocs.io/ and https://yamllint.readthedocs.io/en/stable/
pip3 install "ansible-lint[yamllint]"
4 - Create the files for ansible and yaml linters:
touch .ansible-lint yamllint
5 - Now, execute the linters on directory project:
ansible-lint
yamllint .
6 - Initialize the molecule test. Run the command below for existing roles. 
molecule init scenario default
7 - To test, simply run this command:
Note: For more details: https://molecule.readthedocs.io/en/latest/getting-started.html
molecule test
