---
description: Um tipo de dados usado para especificar os atributos de acesso de segurança no Registro.
title: REGSAM (Winnt.h)
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
ms.openlocfilehash: e202e615561ce0c51f44fc39726d8ab864afc2b5e1bcbbe5612edbb74c476c29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820416"
---
# <a name="regsam"></a>REGSAM

Um tipo de dados usado para especificar os atributos de acesso de segurança no Registro.



| Constante                                                                                                                                                                                   | Descrição                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**KEY \_ ALL \_ ACCESS**</dt> </dl>                          | Combinação de ****KEY \_ QUERY \_ VALUE***, ****KEY \_ ENUMERATE \_ SUB \_ KEYS***, ***KEY \_ NOTIFY***, ***KEY \_ CREATE SUB \_ \_ KEY**** , ***KEY \_ CREATE \_ LINK*** e ***KEY \_ SET \_ VALUE**** access.<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**KEY \_ CREATE \_ LINK**</dt> </dl>                       | Permissão para criar um link simbólico.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**CHAVE \_ CRIAR \_ \_ SUB-CHAVE**</dt> </dl>             | Permissão para criar subkeys.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**\_SUB-CHAVES DE \_ ENUMERAÇÃO DE \_ CHAVE**</dt> </dl> | Permissão para enumerar subkeys.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**KEY \_ EXECUTE**</dt> </dl>                                    | Permissão para acesso de leitura.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**NOTIFICAÇÃO \_ DE CHAVE**</dt> </dl>                                       | Permissão para notificação de alteração.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**VALOR \_ DA CONSULTA DE \_ CHAVE**</dt> </dl>                       | Permissão para consultar dados de sub-chave.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**LEITURA \_ DE CHAVE**</dt> </dl>                                             | Combinação de acesso DE \_ SUB KEYS*KEY QUERY \_ VALUE***, ****KEY \_ ENUMERATE SUB \_ \_ KEYS*** e ***KEY \_ NOTIFY****.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**VALOR \_ DO CONJUNTO DE \_ CHAVES**</dt> </dl>                             | Permissão para definir dados de sub-chave.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**GRAVAÇÃO \_ DE CHAVE**</dt> </dl>                                          | Combinação de acesso ***KEY \_ SET \_ VALUE*** e ***KEY \_ CREATE SUB \_ \_ KEY****.<br/>                                                                                                                |



## <a name="remarks"></a>Comentários

Um **valor REGSAM** pode ser um ou mais dos valores listados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt.h</dt> </dl> |



 

 




