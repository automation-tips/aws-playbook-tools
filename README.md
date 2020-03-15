# aws-playbook-tools

## 必須パッケージ

- boto
- boto3
- ansible

## セットアップ

### 必須パッケージのインストール

```
$ pip isntall boto boto3 ansible
```

### キーペアの設定

```
$ vi ec2-provisioning/host_vars/localhost.yml

---
my_vars:
  # AWSに登録したキーペア名を入力
  ec2:
    key_name: xxxxxx
---

```

### 秘密鍵の設定

```
$ vi ec2-provisioning/ansible.cfg

---
.
.
.
private_key_file=~/.ssh/xxxxxx.pem  ← ここに秘密鍵を指定
.
---
```
