---
title: Interface IMediaRenderer
description: Encapsula os métodos e eventos necessários para representar um dispositivo DMR (processador de mídia digital) DLNA.
ms.assetid: FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB
keywords:
- API de streaming de mídia da interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, descrita
topic_type:
- apiref
api_name:
- IMediaRenderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 363db88b67d29d92b1e79516056f5fa8e78ca22e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917258"
---
# <a name="imediarenderer-interface"></a>Interface IMediaRenderer

Encapsula os métodos e eventos necessários para representar um dispositivo DMR (processador de mídia digital) DLNA.

## <a name="members"></a>Membros

A interface **IMediaRenderer** herda de [**IBasicDevice**](ibasicdevice.md). **IMediaRenderer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMediaRenderer** tem esses métodos.



| Método                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActionInformation**](imediarenderer-actioninformation.md)                                 | Recupera informações sobre quais métodos podem ser invocados atualmente no DMR.<br/>                                                                                                                                                                                                                                                                                    |
| [**Adicionar \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate)        | Registra um manipulador de eventos para o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                          |
| [**Adicionar \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate)        | Registra um manipulador de eventos para o evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                          |
| [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)                                           | Consulta o DMR de forma assíncrona para determinar se o áudio está com mudo ou mudo no momento.<br/>                                                                                                                                                                                                                                                                               |
| [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)             | Consulta o DMR de forma assíncrona para recuperar informações de posição.<br/>                                                                                                                                                                                                                                                                                                  |
| [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)           | Consulta o DMR de forma assíncrona para recuperar informações de transporte.<br/>                                                                                                                                                                                                                                                                                                 |
| [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)                                       | Consulta o DMR de forma assíncrona para seu nível de volume de áudio atual.<br/>                                                                                                                                                                                                                                                                                                |
| [**IsAudioSupported**](imediarenderer-isaudiosupported.md)                                   | Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de áudio.<br/>                                                                                                                                                                                                                                                                             |
| [**IsImageSupported**](imediarenderer-isimagesupported.md)                                   | Recupera um valor que indica se o DMR é capaz de exibir imagens.<br/>                                                                                                                                                                                                                                                                                 |
| [**IsVideoSupported**](imediarenderer-isvideosupported.md)                                   | Recupera um valor que indica se o DMR é capaz de reproduzir conteúdo de vídeo.<br/>                                                                                                                                                                                                                                                                             |
| [**PauseAsync**](imediarenderer-pauseasync.md)                                               | Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                                                                            |
| [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync)                                                 | Instrui o DMR de forma assíncrona a reproduzir o conteúdo que foi especificado chamando o método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) .<br/>                       |
| [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync)                                   | Instrui o DMR de forma assíncrona a reproduzir o conteúdo que foi especificado chamando o método [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync), [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)ou [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync) na taxa especificada.<br/> |
| [**Remover \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate)  | Cancela o registro de um manipulador de eventos para o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) .<br/>                                                                                                                                                                                                                                                        |
| [**Remover \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)  | Cancela o registro de um manipulador de eventos para o evento [**TransportParametersUpdate**](transportparametersupdate.md) .<br/>                                                                                                                                                                                                                                                        |
| [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)                                                 | Instrui o DMR de forma assíncrona a buscar um deslocamento de tempo específico.<br/>                                                                                                                                                                                                                                                                                             |
| [**SetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setmuteasync)                                           | Instrui o DMR de forma assíncrona para ativar mudo ou mudo do áudio. <br/>                                                                                                                                                                                                                                                                                             |
| [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) | Instrui o DMR de forma assíncrona a preparar o conteúdo especificado para reprodução após a conclusão da reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                      |
| [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync)           | Instrui o DMR de forma assíncrona a preparar o fluxo de mídia especificado para reprodução após a conclusão da reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                 |
| [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync)                 | Instrui o DMR de forma assíncrona a preparar o conteúdo identificado pelo URI especificado para reprodução depois que o conteúdo atual tiver terminado a reprodução.<br/>                                                                                                                                                                                                                |
| [**SetSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefrommediasourceasync)         | Instrui o DMR assincronamente a preparar o conteúdo especificado para reprodução.<br/>                                                                                                                                                                                                                                                                                    |
| [**SetSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromstreamasync)                   | Instrui o DMR assincronamente a preparar o fluxo de mídia especificado para reprodução.<br/>                                                                                                                                                                                                                                                                               |
| [**SetSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setsourcefromuriasync)                         | Instrui o DMR de forma assíncrona a preparar o conteúdo identificado pelo URI especificado para reprodução.<br/>                                                                                                                                                                                                                                                              |
| [**SetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setvolumeasync)                                       | Define o nível de volume de áudio no DMR de forma assíncrona com o valor especificado.<br/>                                                                                                                                                                                                                                                                                     |
| [**StopAsync**](imediarenderer-stopasync.md)                                                 | Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

