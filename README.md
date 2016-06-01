## Ansible環境 ＆ WP構築手順
## index

### Vagrantで環境を作成
1. お決まりの、vagrant up
1. CentOS7が立つまで、Ansibleのこと話します。AnsibleがホストPCにインストールされていない人は、インストールしてください。

```
$ brew install ansible
$ ansible --version
```

### いよいよAnsibleを実行
1. playbookについて
1. hostsについて
1. 