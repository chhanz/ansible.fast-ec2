# ansible.fast-ec2
Provisioning EC2 instance and deploy APP for Demo.   
   
# Requirements
AWS CLI 를 통해 `$ aws configure` 가 완료되어 있어야합니다.   
```
~/.aws/config
~/.aws/credentials
```
   
아래와 같이 Ansible Collention 가 사전에 설치 되어 있어야합니다.   
```
$ ansible-galaxy collection list
Collection                    Version
----------------------------- -------
amazon.aws                    6.5.0
community.docker              3.4.9
...
```
# Role Variables
아래 변수를 사용하여 인스턴스 이름을 지정 할 수 있습니다.   
```
ec2_instnace_name: "Demo"
```
   
아래 변수를 사용하여 생성 할 인스턴스의 수를 지정 할 수 있습니다.   
```
ec2_instance_count: "2"
```
   
아래 변수를 통해 사용할 Keypair 를 지정 할 수 있습니다.   
```
ec2_instnace_key_name: "demo-key"
```
   
아래 변수를 통해 인스턴스가 생성될 subnet id 를 지정 할 수 있습니다.   
```
ec2_instnace_subnet_id: "subnet-1234567890abcdef"
```
   
아래 변수를 통해 인스턴스 유형을 지정 할 수 있습니다.   
```
ec2_instnace_type: "c5.large"
```
   
아래 변수를 통해 인스턴스에서 사용할 보안 그룹을 지정 할 수 있습니다.   
```
ec2_instnace_sg: "sg-1234567890abcdef"
```
   
아래 변수를 통해 인스턴스 생성에 사용 할 AMI 를 지정 할 수 있습니다.   
```
ec2_instnace_ami: "ami-09af799f87c7601fa"
```
   
아래 변수를 통해 인스턴스 프로파일을 지정 할 수 있습니다.   
```
ec2_instance_profile: "default"
```
   
# Example Playbook
```
$ ansible-playbook -i inventory demo-playbook.yml
```
   