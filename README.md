Parameters:
  SubnetId:
    Type: String
    Default: add-your-value-here
  SecurityGroupId:
    Type: String
    Default: add-your-value-here
  ImageId:
    Type: String
    Default: add-your-value-here

Resources:
  Ec2Instance: 
    Type: AWS::EC2::Instance
    Properties:
      InstanceType: t3.micro
      ImageId: !Ref ImageId
      SubnetId: !Ref SubnetId
      SecurityGroupIds:
      - !Ref SecurityGroupId
