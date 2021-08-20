---
description: Evento de alteração do catálogo Winsock para uma operação de remoção do LSP (provedor de serviços em camadas).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0ac13a5404dcbbfe5fb5f5d8c2a5f17d43edeb72ba135abfc7e85ad9e5227a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321588"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE

> [!Note]  
> Provedores de serviços em camadas foram preterido. Começando com Windows 8 e Windows Server 2012, use [Windows De filtragem.](../fwp/windows-filtering-platform-start-page.md)

 

O **evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE** é um evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviços em camadas).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome LSP* 
</dt> <dd>

O nome do LSP conforme obtido do membro **szProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.

</dd> <dt>

*Catálogo* 
</dt> <dd>

O catálogo winsock (32 bits ou 64 bits) em que o LSP está sendo removido. Esse é um valor inteiro que é 32 ou 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

O nome do arquivo do módulo do aplicativo que está fazendo a chamada de remoção do LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

O valor guid do provedor de transporte Winsock do que o LSP está sendo removido.

</dd> <dt>

*Categoria* 
</dt> <dd>

O **membro dwCatalogEntryId** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE** é rastreado para uma operação de remoção de LSP quando uma entrada de protocolo é removida do catálogo Winsock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle do rastreamento winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de alterações do catálogo winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
