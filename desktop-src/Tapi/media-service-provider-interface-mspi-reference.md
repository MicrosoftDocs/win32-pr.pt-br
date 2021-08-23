---
description: Este documento descreve as interfaces que fornecem métodos que permitem que um MSP interaja com o ambiente de Telefonia da Microsoft e permita que um aplicativo TAPI 3 use controles de mídia MSPs.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referência de MSPI (Interface do Provedor de Serviços de Mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94ce02312a7c94a7bc2b805a6c73c263546d9cb3f21bbe795d92a91b1010a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404746"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referência de MSPI (Interface do Provedor de Serviços de Mídia)

Este documento descreve as interfaces que fornecem métodos que permitem que um MSP interaja com o ambiente de Telefonia da Microsoft e permita que um aplicativo TAPI 3 use controles de mídia do MSP.



| Interfaces de interface do provedor de serviços de mídia      | Descrição                                                                                                                                                                            | Necessário? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Exposto somente ao TAPI. Interface MSP principal para a DLL tapi. TAPI 3 chama **CoCreateInstance** nessa interface para criar o objeto MSP.                                               | Sim       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Exposto a aplicativos. Fornece métodos que permitem que um aplicativo recupere informações em um fluxo, inicie, pause ou pare e selecione ou desmarque terminais em um fluxo. | Sim       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Exposto a aplicativos. Fornece métodos que permitem que um aplicativo crie ou remova fluxos.                                                                                       | Sim       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Exposto a aplicativos. Interface do enumerador [**para ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                                                                                        | Sim       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Exposto a aplicativos. Fornece métodos que permitem que um aplicativo recupere informações em um substream, inicie, pause ou pare e selecione ou desmarque terminais.          | Opcional  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Exposto a aplicativos. Fornece métodos que permitem que um aplicativo crie ou remova substreams.                                                                                    | Opcional  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Exposto a aplicativos. Interface do enumerador [**para ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)                                                                                                  | Opcional  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Exposto a aplicativos. Obtém informações sobre o [objeto Terminal](terminal-object.md), como chamada de terminal e mídia com suporte.                                                    | Sim       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Exposto a aplicativos. Fornece métodos para consultar em terminais disponíveis e criar terminais adicionais.                                                                             | Sim       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Exposto a aplicativos. Recupera informações sobre classes de terminal e superclasses que podem ser plugáveis; deriva da interface [**ITTerminalSupport.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)           | Sim       |



 

## <a name="media-service-provider-interface-types"></a>Tipos de interface do provedor de serviços de mídia

-   [**EVENTO DE \_ ENDEREÇO \_ MSP**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**EVENTO DE \_ CHAMADA do \_ MSP**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**EVENTO \_ MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**INFORMAÇÕES DE EVENTO \_ DO \_ MSP**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface do Provedor de Serviços de Mídia (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
