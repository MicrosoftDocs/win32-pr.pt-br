---
description: O funcionamento adequado dos componentes TAPI requer a configuração do ambiente de comunicação em um computador.
ms.assetid: 3df3d974-629e-4d78-b97d-b8121b185309
title: Inicialização TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973d67931fb9f33751fedc638ab77021d3d3d34c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788044"
---
# <a name="tapi-initialization"></a>Inicialização TAPI

O funcionamento adequado dos componentes TAPI requer a configuração do ambiente de comunicações em um computador da seguinte maneira:

-   A [instalação](installation.md) é executada quando o software ou hardware é adicionado pela primeira vez ao computador. Os procedimentos detalhados dependem do sistema operacional e do próprio software.
-   A [inicialização primária](primary-initialization.md) cria os objetos e os caminhos de comunicação.
-   A [negociação de versão](version-negotiation.md) garante que os componentes TAPI poderão trocar dados.
-   O [inventário de recursos](resource-inventory.md) recupera informações relacionadas a dispositivos disponíveis para uso por um aplicativo TAPI.
-   A [notificação de eventos](event-notification.md) especifica como a TAPI e os provedores de serviço passam resultados de operação assíncrona e informações de alteração de estado para o aplicativo.

## <a name="summary-of-related-reference-pages"></a>Resumo das páginas de referência relacionadas



| Funções TAPI 2. x                                        | Descrição                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)     | Configura o ambiente de telefonia, retorna o identificador do aplicativo e a contagem de dispositivos.                                                   |
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)         | Obtém recursos do dispositivo, como a versão TAPI ou os tipos de mídia com suporte.                                                          |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) | Obtém os recursos de endereço, como se há suporte para o parque de chamadas.                                                                |
| [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen)                     | Notifica a TAPI que o aplicativo usará a linha e de que maneira.                                                       |
| [**lineGetMessage**](/windows/win32/api/tapi/nf-tapi-linegetmessage)         | Retorna a próxima mensagem TAPI que é enfileirada para entrega a um aplicativo que está usando o mecanismo de notificação do manipulador de eventos |



 



| Interfaces ou métodos TAPI 3. x                                                | Descrição                                                                                                                                |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize)                               | Configura o ambiente de telefonia.                                                                                                             |
| [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)               | Enumera os endereços disponíveis no momento.                                                                                                  |
| [**ITTAPI:: obter \_ endereços**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses)                        | Cria uma coleção de endereços disponíveis no momento. Fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic. |
| [**Evento ITTAPIEventNotification::**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)       | Determina a resposta a uma notificação de evento assíncrono. Implementado pelo aplicativo, invocado pela TAPI.                                |
| [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter)                    | Define a máscara de filtro de eventos, que notifica a TAPI quais eventos o aplicativo requer.                                                     |
| [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) | Instrui a TAPI a passar as sessões de entrada do aplicativo para um endereço especificado e um conjunto de tipos de mídia.                                   |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                                      | Permite que um aplicativo Descubra os recursos de suporte de mídia para um endereço.                                                           |



 

 

 
