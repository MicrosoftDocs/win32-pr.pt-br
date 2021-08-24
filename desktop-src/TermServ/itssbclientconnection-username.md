---
title: Propriedade UserName ITsSbClientConnection
description: Recupera um valor que indica o nome do usuário que iniciou a conexão.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Propriedade UserName Serviços de Área de Trabalho Remota
- A propriedade UserName Serviços de Área de Trabalho Remota , interface ITsSbClientConnection
- Interface ITsSbClientConnection Serviços de Área de Trabalho Remota , propriedade UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6961e6c911b24df2e6c3adbea14b31a2ce8e5a66a9be9082357db957e646a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511326"
---
# <a name="itssbclientconnectionusername-property"></a>Propriedade ITsSbClientConnection::UserName

Recupera um valor que indica o nome do usuário que iniciou a conexão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um nome de usuário. Quando terminar de usar a cadeia de caracteres, livre-a chamando a [**função SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

