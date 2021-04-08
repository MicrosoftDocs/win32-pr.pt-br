---
title: Interfaces de streaming de mídia
description: A API de streaming de mídia fornece as seguintes interfaces.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6cdb1893af3170ae9ec5989498a007230992361
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917879"
---
# <a name="media-streaming-interfaces"></a>Interfaces de streaming de mídia

A [API de streaming de mídia](media-streaming-api-portal.md) fornece as seguintes interfaces.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                 | Descrição                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Representa um [**IBasicDevice**](ibasicdevice.md) ativo que está associado a um dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Fornece métodos estáticos para a criação de objetos [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) . <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Encapsula os métodos e eventos necessários para recuperar uma lista de renderizadores de mídia digital (DMRs) e/ou servidores de mídia digital (DMSs) armazenados em cache, ou para localizar de forma assíncrona o DMRs e/ou o DMSs que estão atualmente na rede.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Encapsula os métodos necessários para fornecer informações sobre o ícone de um dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Representa um par de objetos [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que é composto por um processador e um servidor.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Encapsula os métodos e eventos necessários para representar um dispositivo DMR (processador de mídia digital) DLNA.<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Encapsula os métodos necessários para fornecer informações sobre quais métodos podem ser invocados atualmente no DMR.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Encapsula os métodos necessários para criar de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer**](imediarenderer.md) .<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Encapsula os métodos necessários para selecionar um fluxo de forma assíncrona.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Encapsula os métodos necessários para fornecer informações sobre as configurações atuais relacionadas ao transporte do DMR. Essas configurações incluem o estado de transporte atual e as informações sobre quais métodos podem ser invocados no momento no DMR.<br/> |



 

 

