# Ansible環境 ＆ WP構築手順


## index

### 1. Vagrantを実行
### 2. Ansible解説＆LAMP環境を構築
### 3. Ansibleを実行
### 4. Wordpressインストール

---

## 1. Vagrantで環境を作成

:OS: CentOS 7.0 64 bit
:ssh pass: vagrant

1-1. `$ vagrant up`  
1-2. `$ vagrant ssh`  
1-3. `$ yum install ansible`

## 2. Ansible解説＆LAMP環境を構築

:mysql_user: vagrant
:db_name: handson

2-1. ディレクトリ構成、各種設定ファイルの解説  
2-2. host_vars設定
2-3. LAMP環境構築用のタスクを作成  
2-4. nginx  
2-5. mysql  
2-6. PHP-FPM

## 3. Ansible実行

3-1. `$ ansible-playbook playbook/site.yml`

## 4. Wordpressインストール
4-1. ansible-playbook playbook/wp.yml
4-2. hostsの設定
4-3. handson.localを確認