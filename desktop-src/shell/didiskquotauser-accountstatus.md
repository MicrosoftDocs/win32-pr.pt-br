---
description: Obtém o status da conta do usuário.
title: Propriedade DIDiskQuotaUser.AccountStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841647"
---
# <a name="didiskquotauseraccountstatus-property"></a>Propriedade DIDiskQuotaUser.AccountStatus

Obtém o status da conta do usuário.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode usar um dos valores a seguir.



| Status            | Valor | Descrição                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | As informações da conta são resolvidas.    |
| dqAcctUnavailable | 1     | As informações da conta não estão disponíveis. |
| dqAcctDeleted     | 2     | A conta foi excluída.           |
| dqAcctInvalid     | 3     | A conta é inválida.                 |
| dqAcctUnknown     | 4     | A conta não pode ser encontrada.            |
| dqAcctUnresolved  | 5     | As informações da conta não estão resolvidas.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




