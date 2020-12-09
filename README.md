# hello-demo role
![ansible ci](https://github.com/y-hashida/ansible-roles_hello-demo/workflows/ansible%20ci/badge.svg)

## 1. 目次

<!-- TOC depthFrom:2 -->

- [1. 目次](#1-目次)
- [2. 概要](#2-概要)
- [3. 動作確認バージョン](#3-動作確認バージョン)
- [4. 使い方 (ansible)](#4-使い方-ansible)
    - [4.1. Role variables](#41-role-variables)
    - [4.2. Example playbook](#42-example-playbook)
- [5. Licence](#5-licence)

<!-- /TOC -->

## 2. 概要

ansible CI デモ用 role

`hello_dest_path` に指定したパスに中身が `Hello, ansible!` と書かれたプレーンテキストファイルを保存します.

<br>

## 3. 動作確認バージョン

<br>

## 4. 使い方 (ansible)

### 4.1. Role variables

```yaml
hello_dest_path: "/tmp/hello.txt"
```

<br>

### 4.2. Example playbook

```yaml
- hosts:
    - servers
  become: True
  roles:
    - { role: ansible-roles_hello-demo, tags: ["hello-demo"] }
```

<br>

## 5. Licence

MIT
