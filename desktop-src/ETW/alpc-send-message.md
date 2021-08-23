---
description: Essa classe é a classe de tipo de evento para ALPC enviar eventos de mensagem. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Classe ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8a3e53e514f80f89f1b1e97c1edde9b86add0db7a29de9443c5a1b48085a40fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070326"
---
# <a name="alpc_send_message-class"></a>Classe de mensagem de \_ envio ALPC \_

Essa classe é a classe de tipo de evento para ALPC enviar eventos de mensagem.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a>Membros

A classe de **\_ \_ mensagem de envio ALPC** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ \_ mensagem de envio ALPC** tem essas propriedades.

<dl> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de mensagem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 




