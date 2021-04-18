---
description: Um MSP (provedor de serviços de mídia) permite que um aplicativo controle a mídia de um mecanismo de transporte específico.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Provedores de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810458"
---
# <a name="media-service-providers"></a>Provedores de serviços de mídia

## <a name="purpose"></a>Finalidade

Um MSP (provedor de serviços de mídia) permite que um aplicativo controle a mídia de um mecanismo de transporte específico. Um MSP é sempre emparelhado com um provedor de serviços de telefonia (TSP).

A MSPI (interface do provedor de serviços de mídia) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo sobre o transporte de mídia durante uma sessão de comunicações. Um MSP manipula os mecanismos específicos do dispositivo e do protocolo, necessários para aplicar esses controles e se comunica com seu TSP ou aplicativo emparelhado por meio do uso dos métodos fornecidos no MSPI.

## <a name="developer-audience"></a>Público de desenvolvedores

É necessário ter familiaridade com com. A experiência de desenvolvimento com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O MSPI permite o desenvolvimento de provedores de serviço de mídia para determinados protocolos ou dispositivos em execução em sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Visão geral](about-the-media-service-provider-msp-.md)<br/>            | Informações gerais sobre a arquitetura e os componentes do MSP.<br/> |
| [Referência](media-service-provider-interface-mspi-reference.md)<br/> | Documentação para as interfaces MSPI.<br/>                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de telefonia da Microsoft](microsoft-telephony-overview.md)
</dt> <dt>

[TAPI 3,1](tapi-3-1-start-page.md)
</dt> <dt>

[Provedores de serviços de telefonia](./telephony-service-providers-start-page.md)
</dt> </dl>

 

