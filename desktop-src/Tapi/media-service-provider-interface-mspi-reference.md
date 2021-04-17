---
description: Este documento descreve as interfaces que fornecem métodos que permitem que um MSP interaja com o ambiente de telefonia da Microsoft e permita que um aplicativo TAPI 3 Use controles de mídia MSPs.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referência de MSPI (interface do provedor de serviços de mídia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759961"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referência de MSPI (interface do provedor de serviços de mídia)

Este documento descreve as interfaces que fornecem métodos que permitem que um MSP interaja com o ambiente de telefonia da Microsoft e permita que um aplicativo TAPI 3 Use os controles de mídia de um MSP.



| Interfaces de interface do provedor de serviços de mídia      | Descrição                                                                                                                                                                            | Necessário? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Exposto somente à TAPI. Interface do MSP principal para a DLL de TAPI. A TAPI 3 chama **CoCreateInstance** nessa interface para criar o objeto msp.                                               | Yes       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Exposto aos aplicativos. Fornece métodos que permitem que um aplicativo recupere informações em um fluxo, inicie, pause ou interrompa e selecione ou desmarque os terminais em um fluxo. | Yes       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Exposto aos aplicativos. Fornece métodos que permitem que um aplicativo crie ou remova fluxos.                                                                                       | Yes       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Exposto aos aplicativos. Interface do enumerador para [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Yes       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Exposto aos aplicativos. Fornece métodos que permitem que um aplicativo recupere informações em um subfluxo, inicie, pause ou interrompa e selecione ou desmarque os terminais.          | Opcional  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Exposto aos aplicativos. Fornece métodos que permitem que um aplicativo crie ou remova subfluxos.                                                                                    | Opcional  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Exposto aos aplicativos. Interface do enumerador para [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Opcional  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Exposto aos aplicativos. Obtém informações sobre o [objeto terminal](terminal-object.md), como suporte a chamadas de terminal e mídia.                                                    | Yes       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Exposto aos aplicativos. Fornece métodos para consultar os terminais disponíveis e criar terminais adicionais.                                                                             | Yes       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Exposto aos aplicativos. Recupera informações sobre as classes de terminal conectável e as superclasses; deriva da interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) .           | Yes       |



 

## <a name="media-service-provider-interface-types"></a>Tipos de interface do provedor de serviço de mídia

-   [**\_evento de endereço MSP \_**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**\_evento de chamada MSP \_**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**\_evento MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**\_informações do evento MSP \_**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[MSPI (interface do provedor de serviços de mídia)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
