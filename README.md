td-agent-conf_ssh
=================

## これは何?
/var/log/auth.log から ssh でログイン失敗したユーザ名と ip アドレスを抽出し、elasticsearch へ登録するコンフィグです

## 特徴
auth.log 中の
```bash
Invalid user etho from 61.182.170.38
```
のようなログからユーザ名と ip アドレスを抽出し,
```bash
"invalid_usr": "etho",
"invalid_host": "61.182.170.38",
```
と JSON 形式で抽出します。

## 使い方
/etc/td-agent/td-agent.conf に記述します
