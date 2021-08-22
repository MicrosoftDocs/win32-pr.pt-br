---
description: Evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051284"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_Evento de \_ \_ redefinição de LSP do Winsock WS2HELP

> [!Note]  
> Os provedores de serviço em camadas são preteridos. começando com Windows 8 e Windows Server 2012, use [Windows plataforma de filtragem](../fwp/windows-filtering-platform-start-page.md).

 

O evento **Winsock \_ ws2help \_ LSP \_ Reset** é um evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Catálogo* 
</dt> <dd>

O catálogo do Winsock (32 bits ou 64 bits) que está sendo redefinido. Este é um valor inteiro que é 32 ou 64.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento **Winsock \_ ws2help \_ LSP \_ Reset** é rastreado para uma operação de LSP (provedor de serviço em camadas) do Winsock quando o catálogo do Winsock é redefinido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
