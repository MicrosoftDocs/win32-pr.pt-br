---
description: Evento de alteração do catálogo winsock para uma operação de desabilitação do LSP (provedor de serviços em camadas).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733126"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE

> [!Note]  
> Provedores de serviços em camadas foram preterido. Começando com Windows 8 e Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).

 

O **evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE** é um evento de alteração de catálogo winsock para uma operação de desabilitação do LSP (provedor de serviços em camadas).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome LSP* 
</dt> <dd>

O nome do LSP conforme obtido do membro **szProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.

</dd> <dt>

*Catálogo* 
</dt> <dd>

O catálogo winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado. Esse é um valor inteiro que é 32 ou 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

O nome do arquivo do módulo do aplicativo que está fazendo com que o LSP desabilite a chamada.

</dd> <dt>

*GUID* 
</dt> <dd>

O valor guid do provedor de transporte Winsock que o LSP está sendo desabilitado.

</dd> <dt>

*Categoria* 
</dt> <dd>

O **membro dwCatalogEntryId** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.

</dd> </dl>

Esse evento não tem parâmetros.

## <a name="remarks"></a>Comentários

O **evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE** é rastreado para uma operação de desabilitação LSP quando uma entrada de protocolo é desabilitada no catálogo winsock.

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

 

 
