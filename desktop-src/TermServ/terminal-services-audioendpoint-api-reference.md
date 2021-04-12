---
title: Serviços de Área de Trabalho Remota referência da API AudioEndpoint
description: Dá suporte a interfaces para registro de ponto de extremidade de áudio e transporte de dados.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, referência de API AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364250"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Serviços de Área de Trabalho Remota referência da API AudioEndpoint

Um *ponto de extremidade de áudio* representa um dispositivo de áudio, uma API de áudio ou qualquer outra fonte de áudio ou coletor, e é usado para enviar dados ou consumir dados do mecanismo de áudio. Um ponto de extremidade de áudio deve ser conectado ao mecanismo de áudio por meio de uma *conexão*, e cada conexão pode ter apenas um ponto de extremidade conectado a ele. Depois que um ponto de extremidade é registrado, o mecanismo de áudio anexa o ponto de extremidade à conexão.

Cada objeto de ponto de extremidade deve implementar as seguintes interfaces:

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) para habilitar o mecanismo de áudio para obter informações sobre o ponto de extremidade.
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) para obter informações sobre o buffer de dados antes de executar uma passagem de processamento e notificar o ponto de extremidade quando a passagem for concluída.
-   A interface [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) ou [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , dependendo se o objeto de ponto de extremidade está capturando ou renderizando áudio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

O mecanismo de áudio usa essas interfaces para obter informações sobre os pontos de extremidade que estão anexados ao mecanismo. A implementação do ponto de extremidade deve fornecer o mecanismo para entregar ou consumir dados do mecanismo, conforme especificado por essas interfaces.

O Serviços de Área de Trabalho Remota API AudioEndpoint dá suporte a tipos de enumeração, interfaces e estruturas.

## <a name="in-this-section"></a>Nesta seção

-   [Serviços de Área de Trabalho Remota tipos de enumeração AudioEndpoint](terminal-services-audioendpoint-enumeration-types.md)
-   [Serviços de Área de Trabalho Remota funções AudioEndpoint](remote-desktop-services-audioendpoint-functions.md)
-   [Serviços de Área de Trabalho Remota interfaces AudioEndpoint](terminal-services-audioendpoint-interfaces.md)
-   [Serviços de Área de Trabalho Remota estruturas AudioEndpoint](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Comentários

O Serviços de Área de Trabalho Remota API AudioEndpoint é para uso em cenários de Área de Trabalho Remota; Não é para aplicativos cliente.

 

 




