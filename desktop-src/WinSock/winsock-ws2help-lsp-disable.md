---
description: Evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).
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
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748863"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_Evento de \_ desabilitação de LSP ws2help do Winsock \_

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O evento **Winsock \_ ws2help \_ LSP \_ Disable** é um evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do LSP* 
</dt> <dd>

O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.

</dd> <dt>

*Catálogo* 
</dt> <dd>

O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado. Este é um valor inteiro que é 32 ou 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

O nome de arquivo do módulo do aplicativo que faz a chamada de desabilitação de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

O valor de GUID do provedor de transporte do Winsock que o LSP está sendo desabilitado.

</dd> <dt>

*Categoria* 
</dt> <dd>

O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.

</dd> </dl>

Este evento não tem parâmetros.

## <a name="remarks"></a>Comentários

O evento **Winsock \_ ws2help \_ LSP \_ Disable** é rastreado para uma operação de desabilitação de LSP quando uma entrada de protocolo está desabilitada no catálogo Winsock.

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

 

 
