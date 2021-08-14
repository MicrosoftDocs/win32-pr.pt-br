---
description: O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acesso à transação (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faafcce45944e37418191254fc5a2b81d00d9248b27ea5e8753fe8e34a734754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520636"
---
# <a name="transaction-access-masks"></a>Máscaras de Acesso à Transação

O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**INFORMAÇÕES \_ DE CONSULTA DE \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



O chamador pode consultar informações de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**INFORMAÇÕES DO \_ CONJUNTO DE \_ TRANSAÇÕES**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



O chamador pode definir informações de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION \_ ENLIST**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



O chamador pode se inscrever nessa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**COMMIT DE \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



O chamador pode fazer commit dessa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**RE \_ ROLLBACK DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



O chamador pode reverter essa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**PROPAGAÇÃO \_ DE TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



O chamador pode propagar essa transação para um gerenciador de recursos superior, como o Coordenador de Transações Distribuídas (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**LEITURA \_ GENÉRICA DA \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



O chamador tem os seguintes privilégios: **STANDARD \_ RIGHTS \_ READ,** **TRANSACTION \_ QUERY \_ INFORMATION** e **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**GRAVAÇÃO \_ GENÉRICA DA \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



O chamador tem os seguintes privilégios: **STANDARD \_ RIGHTS \_ WRITE,** **TRANSACTION SET \_ \_ INFORMATION,** **TRANSACTION COMMIT, TRANSACTION \_ ENLIST,** **TRANSACTION \_ ROLLBACK,** **TRANSACTION \_ PROPAGATE** e **SYNCHRONIZE**. **\_**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



O chamador tem os seguintes privilégios: **STANDARD \_ RIGHTS \_ EXECUTE,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ROLLBACK** e **SYNCHRONIZE.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



O chamador tem o seguinte privilégio: **DIREITOS \_ PADRÃO \_ OBRIGATÓRIOS,** **LEITURA \_ GENÉRICA \_** DE TRANSAÇÃO, **GRAVAÇÃO \_ GENÉRICA \_** DE TRANSAÇÃO e TRANSACTION GENERIC **\_ \_ EXECUTE.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**DIREITOS DO \_ GERENCIADOR DE RECURSOS DE \_ \_ TRANSAÇÃO**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



O chamador tem os seguintes privilégios: **TRANSACTION \_ GENERIC \_ READ, STANDARD** RIGHTS WRITE, TRANSACTION SET **\_ \_ INFORMATION,** **TRANSACTION \_ \_** **\_ ROLLBACK,** **TRANSACTION \_ ENLIST,** **TRANSACTION \_ PROPAGATE** e **SYNCHRONIZE**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

É recomendável que os gerenciadores de recursos, ao se inscrever em uma transação, especifiquem **TRANSACTION RESOURCE \_ MANAGER \_ \_ RIGHTS** ao abrir uma transação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




