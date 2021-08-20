---
title: Classe MediaRenderer
description: Implementa a interface IMediaRenderer que representa um dispositivo DMR (processador de mídia digital DLNA).
ms.assetid: bac7898f-1334-4e28-92c7-6de464884eaf
keywords:
- API de streaming de mídia de classe MediaRenderer
- API de streaming de mídia de classe MediaRenderer, descrita
topic_type:
- apiref
api_name:
- MediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b003c0c24838b77e044fc0bf14beaac0c97eeebd64415d74ca77bd2e8a44a105
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870823"
---
# <a name="mediarenderer-class"></a>Classe MediaRenderer

Implementa a interface [**IMediaRenderer**](imediarenderer.md) que representa um dispositivo DMR (processador de mídia digital DLNA).

**MediaRenderer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MediaRenderer** tem esses métodos.



| Método                                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adicionar \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828962(v=vs.85))        | Registra um manipulador de eventos para o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**Adicionar \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828963(v=vs.85))        | Registra um manipulador de eventos para o evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                       |
| [**GetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828964(v=vs.85))                                           | Consulta o DMR de forma assíncrona para determinar se o áudio está com mudo ou mudo no momento.<br/>                                                                                                                                                                                                                                                                            |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/legacy/hh828965(v=vs.85))             | Consulta o DMR de forma assíncrona para recuperar informações de posição.<br/>                                                                                                                                                                                                                                                                                               |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/legacy/hh828966(v=vs.85))           | Consulta o DMR de forma assíncrona para recuperar informações de transporte.<br/>                                                                                                                                                                                                                                                                                              |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828967(v=vs.85))                                       | Consulta o DMR de forma assíncrona para seu nível de volume de áudio atual.<br/>                                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](mediarenderer-pauseasync.md)                                               | Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                                                                         |
| [**PlayAsync**](/previous-versions/windows/desktop/legacy/hh828972(v=vs.85))                                                 | Instrui o DMR de forma assíncrona a reproduzir o conteúdo que foi especificado chamando o método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) .<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/legacy/hh828973(v=vs.85))                                   | Instrui o DMR de forma assíncrona a reproduzir o conteúdo que foi especificado chamando o método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85)), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85)) na taxa especificada.<br/> |
| [**Remover \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828974(v=vs.85))  | Cancela o registro de um manipulador de eventos para o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**Remover \_ TransportParametersUpdate**](/previous-versions/windows/desktop/legacy/hh828975(v=vs.85))  | Cancela o registro de um manipulador de eventos para o evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                     |
| [**SeekAsync**](/previous-versions/windows/desktop/legacy/hh828976(v=vs.85))                                                 | Instrui o DMR de forma assíncrona a buscar um deslocamento de tempo específico.<br/>                                                                                                                                                                                                                                                                                          |
| [**SetMuteAsync**](/previous-versions/windows/desktop/legacy/hh828977(v=vs.85))                                           | Instrui o DMR de forma assíncrona para ativar mudo ou mudo do áudio.<br/>                                                                                                                                                                                                                                                                                           |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828978(v=vs.85)) | Instrui o DMR de forma assíncrona a preparar o conteúdo especificado para reprodução após a conclusão da reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                   |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828979(v=vs.85))           | Instrui o DMR de forma assíncrona a preparar o fluxo de mídia especificado para reprodução após a conclusão da reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                              |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828980(v=vs.85))                 | Instrui o DMR de forma assíncrona a preparar o conteúdo identificado pelo URI especificado para reprodução depois que o conteúdo atual tiver terminado a reprodução.<br/>                                                                                                                                                                                                             |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/legacy/hh828981(v=vs.85))         | Instrui o DMR assincronamente a preparar o conteúdo especificado para reprodução.<br/>                                                                                                                                                                                                                                                                                 |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/legacy/hh828982(v=vs.85))                   | Instrui o DMR de forma assíncrona a preparar o fluxo de mídia especificado para reprodução após a conclusão da reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                              |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/legacy/hh828983(v=vs.85))                         | Instrui o DMR de forma assíncrona a preparar o conteúdo identificado pelo URI especificado para reprodução.<br/>                                                                                                                                                                                                                                                           |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/legacy/hh828984(v=vs.85))                                       | Define o nível de volume de áudio no DMR de forma assíncrona com o valor especificado.<br/>                                                                                                                                                                                                                                                                                  |
| [**StopAsync**](mediarenderer-stopasync.md)                                                 | Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                                                                          |



 

### <a name="properties"></a>Propriedades

A classe **MediaRenderer** tem essas propriedades.



| Propriedade                                                                | Tipo de acesso          | Descrição                                                                                 |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------|
| [**ActionInformation**](mediarenderer-actioninformation.md)<br/> | Somente leitura<br/> | Obtém informações sobre quais métodos podem ser invocados atualmente no DMR.<br/>        |
| [**IsAudioSupported**](mediarenderer-isaudiosupported.md)<br/>   | Somente leitura<br/> | Obtém um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.<br/> |
| [**IsImageSupported**](mediarenderer-isimagesupported.md)<br/>   | Somente leitura<br/> | Obtém um valor que indica se o DMR é capaz de exibir imagens.<br/>     |
| [**IsVideoSupported**](mediarenderer-isvideosupported.md)<br/>   | Somente leitura<br/> | Obtém um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.<br/> |



 

 

