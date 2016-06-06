# Ansible環境 ＆ WP構築手順


## index

### 1. Vagrantで環境を作成
### 2. Ansible実行の前に
### 3. ゲスト環境にAnsibleをインストール
### 4. プレイブックを実行
### 5. Wordpressインストール

---

## 1. Vagrantで環境を作成
1. vagrant up
1. CentOS7が立つまで、諸々話します！

## 2. Ansible実行の前に
1. 各種ディレクトリと役割
1. プレイブック、インベントリ（hosts）、
1. プロダクション、ステージング管理

## 3. ゲスト環境にAnsibleをインストール
1. yum -y update
1. sudo yum install -y epel-release
1. sudo yum install -y sshpass
1. sudo yum install -y python-devel
1. sudo yum install ansible

## 4. プレイブックを実行
1. ansible-playbook playbook/site.yml -i hosts/local

## 5. Wordpressインストール
1. ansible-playbook playbook/wp.yml -i hosts/local
