---
description: O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acesso à transação (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faafcce45944e37418191254fc5a2b81d00d9248b27ea5e8753fe8e34a734754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520636"
---
# <a name="transaction-access-masks"></a>Máscaras de acesso à transação

O KTM define as seguintes máscaras de acesso à transação a serem usadas ao abrir uma transação.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informações de consulta de transação \_**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



O chamador pode consultar informações de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_informações do conjunto de transações \_**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



O chamador pode definir informações de transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscrição de transação \_**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



O chamador pode se inscrever nessa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**confirmação de transação \_**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



O chamador pode confirmar essa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**reversão de transação \_**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



O chamador pode reverter essa transação.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagação de transações \_**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



O chamador pode propagar essa transação para um Gerenciador de recursos superior, como o Coordenador de Transações Distribuídas (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_leitura genérica da transação \_**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ leitura de direitos padrão**, **\_ \_ informações de consulta de transação** e **sincronização**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_gravação genérica de transação \_**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de transações**, **\_ confirmação de transação**, **\_ inscrição de transação**, **\_ reversão de transação**, **\_ propagação de transações** e **sincronização**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_execução genérica da transação \_**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ execução de direitos padrão**, **\_ confirmação de transação**, **\_ reversão de transação** e **sincronização**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_todos os \_ acessos à transação**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



O chamador tem o seguinte privilégio: **\_ direitos padrão \_ necessários**, **\_ \_ leitura genérica de transação**, **\_ \_ gravação genérica de transação** e **\_ \_ execução genérica de transação**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_direitos do \_ Gerenciador de recursos de transação \_**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



O chamador tem os seguintes privilégios: **\_ \_ leitura genérica de transação**, **\_ \_ gravação de direitos padrão**, **\_ \_ informações de conjunto de transações**, **\_ reversão de transação**, **\_ inscrição de transação**, **\_ propagação de transações** e **sincronização**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

É recomendável que os gerenciadores de recursos, ao se enlistar em uma transação, especifiquem os direitos do Gerenciador de recursos de transação ao abrir uma transação. **\_ \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




