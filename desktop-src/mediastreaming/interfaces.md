---
title: Interfaces de streaming de mídia
description: A API de Streaming de Mídia fornece as interfaces a seguir.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb21c5c17502c887f78fa223ec2a2f8f814d3998bb75b81812eb4de9919f7342
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972185"
---
# <a name="media-streaming-interfaces"></a>Interfaces de streaming de mídia

A [API de Streaming de Mídia](media-streaming-api-portal.md) fornece as interfaces a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                 | Descrição                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Representa um [**IBasicDevice**](ibasicdevice.md) ativo associado a um dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Fornece métodos estáticos para criar [**objetos IActiveBasicDevice.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Encapsula os métodos e eventos necessários para recuperar uma lista de DMRs (Renderizações de Mídia Digital) e/ou DMSs (Servidores de Mídia Digital) armazenados em cache ou para encontrar as DMRs e/ou DMSs que estão atualmente na rede.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Encapsula os métodos necessários para fornecer informações sobre o ícone de um dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Representa um par de [**objetos ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que é composto por um renderador e um servidor.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Encapsula os métodos e eventos necessários para representar um dispositivo DMR (Renderização de Mídia Digital) DLNA.<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Encapsula os métodos necessários para fornecer informações sobre quais métodos podem ser invocados atualmente na DMR.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Encapsula os métodos necessários para criar de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer.**](imediarenderer.md)<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Encapsula os métodos necessários para selecionar um fluxo de forma assíncrona.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Encapsula os métodos necessários para fornecer informações sobre as configurações atuais relacionadas ao transporte da DMR. Essas configurações incluem o estado de transporte atual e informações sobre quais métodos podem ser invocados atualmente na DMR.<br/> |



 

 

