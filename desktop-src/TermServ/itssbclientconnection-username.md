---
title: Propriedade de nome de usuário ITsSbClientConnection
description: Recupera um valor que indica o nome do usuário que iniciou a conexão.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Propriedade de nome de usuário Serviços de Área de Trabalho Remota
- Propriedade UserName Serviços de Área de Trabalho Remota, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, Propriedade UserName
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
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295877"
---
# <a name="itssbclientconnectionusername-property"></a>Propriedade ITsSbClientConnection:: UserName

Recupera um valor que indica o nome do usuário que iniciou a conexão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um nome de usuário. Quando você terminar de usar a cadeia de caracteres, libere-a chamando a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

