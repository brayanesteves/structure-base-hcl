# Command lines execute (Example)
1) packer init .
2) packer validate .
3) # Validate templete
    packer validate \
    -var "ami_name=custom-ami-12022024" \
    -var "vpc_id=vpc-0de6dcebcb1d1e89e" \
    -var "subnet_id=subnet-060ff58f504f124dd" \
    -var "ssh_public_key=${cat ~/.ssh/id_ed25519.pub}" custom-ami.pkr.hcl
4) export AWS_PROFILE=personal
5) # Build templete
    packer build \
    -var "ami_name=custom-ami-12022024" \
    -var "vpc_id=vpc-0de6dcebcb1d1e89e" \
    -var "subnet_id=subnet-060ff58f504f124dd" \
    -var "ssh_public_key=${cat ~/.ssh/id_ed25519.pub}" custom-ami.pkr.hcl