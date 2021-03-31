---
description: O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de transações (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acesso do Gerenciador de transações (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828113"
---
# <a name="transaction-manager-access-masks"></a>Máscaras de acesso do Gerenciador de transações

O KTM define as seguintes máscaras de acesso à inscrição a serem usadas ao abrir um Gerenciador de transações (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**informações de consulta TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



O chamador pode consultar informações sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**informações de definição de TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



O chamador pode definir informações sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**recuperação de transacionator \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



O chamador pode recuperar este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**renomeação de TransactionManager \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



O chamador pode renomear uma instância de TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**\_criar RM de transação \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



O chamador pode criar um Gerenciador de recursos associado a este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**transação de associação TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Esse valor é reservado.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**leitura genérica TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ as informações de consulta de leitura e transacionator** de **\_ direitos \_ padrão** .


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**gravação genérica TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **Transações de \_ definição \_ de TransactionManager**, **\_ renomeação** de **transacionator, \_ recuperação** e **TransactionManager \_ criar \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**execução genérica TransactionManager \_ \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



O chamador tem o seguinte privilégio: **direitos padrão são \_ \_ executados**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**\_todos os acessos de TRANSacçãomanager \_**
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
| parâmetro<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




