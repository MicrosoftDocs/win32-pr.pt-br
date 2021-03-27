---
description: Um tipo de dados usado para especificar os atributos de acesso de segurança no registro.
title: REGSAM (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970830"
---
# <a name="regsam"></a>REGSAM

Um tipo de dados usado para especificar os atributos de acesso de segurança no registro.



| Constante                                                                                                                                                                                   | Descrição                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**CHAVE de \_ todo o \_ acesso**</dt> </dl>                          | Combinação de * * * * valor de consulta de chave \_ \_ * * * *, * * * * chave enumerar subchaves \_ * * * * \_ \_ , * * * * notificação de chave * * * *, * * * * \_ chave \_ criar \_ \_ subchave * \_ \_ \_ \_ * * *, * * * * chave de criação de link * * * *<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_link de criação de chave \_**</dt> </dl>                       | Permissão para criar um link simbólico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**\_ \_ sub chave de criação de chave \_**</dt> </dl>             | Permissão para criar subchaves.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**\_sub- \_ \_ chaves enumerar chave**</dt> </dl> | Permissão para enumerar subchaves.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**\_executar chave**</dt> </dl>                                    | Permissão para acesso de leitura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**notificação de chave \_**</dt> </dl>                                       | Permissão para notificação de alteração.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**\_valor da consulta de chave \_**</dt> </dl>                       | Permissão para consultar dados de subchave.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**leitura de chave \_**</dt> </dl>                                             | Combinação de * * * * valor de consulta de chave \_ \_ * * * *, * * * * chave enumerar subchaves \_ * * * * \_ \_ e * * * * notificação de chave * * * \_ * acesso.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**\_valor do conjunto de chaves \_**</dt> </dl>                             | Permissão para definir os dados da subchave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**gravação de chave \_**</dt> </dl>                                          | Combinação de * * * * valor de conjunto de chaves \_ \_ * * * * e * * * * chave \_ Create \_ sub \_ Key * * * * Access.<br/>                                                                                                                |



## <a name="remarks"></a>Comentários

Um valor de **REGSAM** pode ser um ou mais dos valores listados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




