---
description: Evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).
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
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797572"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>\_Evento de \_ remoção de LSP ws2help do Winsock \_

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O evento **Winsock \_ ws2help \_ LSP \_ Remove** é um evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do LSP* 
</dt> <dd>

O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.

</dd> <dt>

*Catálogo* 
</dt> <dd>

O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo removido. Este é um valor inteiro que é 32 ou 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

O nome de arquivo do módulo do aplicativo que faz a chamada de remoção de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

O valor de GUID do provedor de transporte do Winsock do qual o LSP está sendo removido.

</dd> <dt>

*Categoria* 
</dt> <dd>

O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento **Winsock \_ ws2help \_ LSP \_ Remove** é rastreado para uma operação de remoção de LSP quando uma entrada de protocolo é removida do catálogo Winsock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 
