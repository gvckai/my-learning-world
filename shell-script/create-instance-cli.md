 aws ec2 run-instances \
        --image-id ami-0055977a6e828a4f4 \
        --instance-type t3.micro \
        --security-group-ids sg-0b3ea593d1d992ac2 \
        --tag-specifications 'ResourceType=instance, Tags=[{Key=Name, Value=roboshop-mongodb}]'