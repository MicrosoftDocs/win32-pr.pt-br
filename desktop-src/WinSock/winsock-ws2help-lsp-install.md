---
description: Evento de alteração de catálogo Winsock para uma operação de instalação do LSP (provedor de serviço em camadas).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922285"
---
# <a name="winsock_ws2help_lsp_install-event"></a>\_Evento de \_ instalação de LSP do Winsock WS2HELP \_

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O evento de **instalação do Winsock \_ ws2help \_ LSP \_** é um evento de alteração de catálogo do Winsock para uma operação de instalação do LSP (provedor de serviço em camadas).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do LSP* 
</dt> <dd>

O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.

</dd> <dt>

*Catálogo* 
</dt> <dd>

O catálogo do Winsock (32 bits ou 64 bits) em que o LSP está sendo instalado. Este é um valor inteiro que é 32 ou 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

O nome de arquivo do módulo do aplicativo que faz a chamada de instalação de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

O valor de GUID do provedor de transporte do Winsock no qual o LSP está sendo instalado.

</dd> <dt>

*Categoria* 
</dt> <dd>

O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento de **instalação do Winsock \_ ws2help \_ LSP \_** é rastreado para uma operação de instalação de LSP quando uma entrada de protocolo é instalada no catálogo do Winsock.

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

 

 
