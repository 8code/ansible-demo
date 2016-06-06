# Ansible環境 ＆ WP構築手順


## index

### 1. Vagrantで環境を作成
### 2. Ansible実行の前に
### 3. ゲスト環境にAnsibleをインストール
### 4. 一旦、プレイブックを実行
### 5. rolesの中身とモジュールの呼び出し
### 6. Wordpressインストール

---

## 1. Vagrantで環境を作成
1-1. `vagrant up`  
1-2. CentOS7が立つまで、諸々話します！

## 2. Ansible実行の前に
2-1. 各種ディレクトリと役割  
2-2. 全体の構成

## 3. ゲスト環境にAnsibleをインストール
3-1. `yum -y update`  
3-2. `sudo yum install -y epel-release`  
3-3. `sudo yum install -y sshpass`  
3-4. `sudo yum install -y python-devel`  
3-5. `sudo yum install ansible`  

## 4. 一旦、プレイブックを実行
4-1. `ansible-playbook playbook/site.yml -i hosts/local`  

## 5. rolesの中身とモジュールの呼び出し
5-1. `roles/{{module}}/tasks/main.yml`  
5-2. 記法とか  
5-3. できる事とか

## 6. Wordpressインストール
6-1. ansible-playbook playbook/wp.yml -i hosts/local
