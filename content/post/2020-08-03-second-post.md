---
title: 二度目の投稿!
date: 2020-08-03
---

## 二度目のテスト投稿

これがテストの記事です。

マークダウンエディタをVSCodeに入れて書いています。

```python

from datetime import datetime
from src.database import db
from flask_marshmallow import Marshmallow
from flask_marshmallow.fields import fields

ma = Marshmallow()

class UserAccountModel(db.Model):

    __tablename__ = 'user_accounts'

    user_id = db.Column(db.Integer, db.ForeignKey('users.id'), primary_key=True)
    account_id = db.Column(db.Integer, db.ForeignKey('accounts.id'), primary_key=True)

class UserAccountSchema(ma.ModelSchema):
    class Meta:
        model = UserAccountModel
    createTime = fields.DateTime('%Y-%m-%dT%H:%M:%S')
    updateTime = fields.DateTime('%Y-%m-%dT%H:%M:%S')

```
