---
description: O KTM define as seguintes máscaras de acesso de inscrições a serem usadas ao abrir um TM (gerenciador de transações).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acesso do Gerenciador de Transações (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfa093f38898ec49a789699fc5c7230612ef744fec78f200021361327d9f714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913896"
---
# <a name="transaction-manager-access-masks"></a>Máscaras de acesso do Gerenciador de Transações

O KTM define as seguintes máscaras de acesso de inscrições a serem usadas ao abrir um TM (gerenciador de transações).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**INFORMAÇÕES DE CONSULTA \_ TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



O chamador pode consultar informações sobre esse TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER \_ SET \_ INFORMATION**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



O chamador pode definir informações sobre esse TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



O chamador pode recuperar esse TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER \_ RENAME**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



O chamador pode renomear uma instância de TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ CREATE \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



O chamador pode criar um gerenciador de recursos associado a esse TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER \_ BIND \_ TRANSACTION**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Esse valor é reservado.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**LEITURA \_ GENÉRICA TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



O chamador tem os seguintes privilégios: **STANDARD \_ RIGHTS \_ READ** e **TRANSACTIONMANAGER \_ QUERY \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**GRAVAÇÃO \_ GENÉRICA TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



O chamador tem os seguintes privilégios: **STANDARD \_ RIGHTS \_ WRITE,** **TRANSACTIONMANAGER \_ SET \_ INFORMATION,** **TRANSACTIONMANAGER \_ RECOVER,** **TRANSACTIONMANAGER \_ RENAME e** **TRANSACTIONMANAGER \_ CREATE \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



O chamador tem o seguinte privilégio: **STANDARD \_ RIGHTS \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Esse valor define todos os bits válidos para um valor de acesso TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




