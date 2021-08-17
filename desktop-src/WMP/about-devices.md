---
title: Sobre dispositivos
description: Sobre dispositivos
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizando dispositivos
- modelo de objeto Windows Media Player, sincronizando dispositivos
- modelo de objeto, sincronizando dispositivos
- Windows Media Player controle de ActiveX, sincronizando dispositivos
- controle de ActiveX, sincronizando dispositivos
- Windows Media Player controle de ActiveX móvel, sincronizando dispositivos
- Windows Media Player Dispositivos móveis, sincronizando
- Sincronizando dispositivos, sobre
- sincronização de dispositivo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66383082bae772b48f913f6bd4615724de8f7b7735e387ba93407a9848f17074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956916"
---
# <a name="about-devices"></a>Sobre dispositivos

Dispositivos portáteis são dispositivos de hardware que os usuários executam para desfrutar do conteúdo de mídia digital quando estão fora do computador. Normalmente, os dispositivos portáteis são operados pela bateria. Alguns dispositivos só podem reproduzir música. Outros dispositivos podem reproduzir vídeo e música.

Alguns dispositivos dão suporte à sincronização automática de conteúdo de mídia digital com o Windows Media Player. Outros dispositivos dão suporte apenas à transferência manual. Você pode determinar se um dispositivo específico dá suporte à sincronização automática chamando [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e, em seguida, inspecionando o valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Se o valor recuperado for **wmpdsManualDevice**, o dispositivo não oferecerá suporte à sincronização automática.

Você pode enumerar os dispositivos conectados ao computador do usuário. Para fazer isso, primeiro use [IWMPSyncServices:: get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) para recuperar a contagem de dispositivos. Em seguida, em um loop, chame [IWMPSyncServices:: GetDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passando o valor de índice apropriado a cada vez. Você pode usar [IWMPSyncDevice:: get \_ conectado](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) para avaliar se um determinado dispositivo está conectado no momento.

Para saber quando os dispositivos se conectam ou se desconectam, você pode receber os eventos **DeviceConnect** e **DeviceDisconnect** . Esses eventos são recebidos por meio da interface **IWMPEvents2** .

A interface **IWMPSyncDevice** fornece métodos adicionais para permitir que você obtenha ou defina informações sobre um dispositivo. Por exemplo:

-   Os métodos **Get \_ FriendlyName** e **Put \_ FriendlyName** permitem recuperar e especificar o nome do dispositivo definido pelo usuário.
-   o método **get \_ devicename** permite que você recupere o nome do dispositivo que os usuários veem no shell do Windows XP.
-   O método **getItemInfo** permite que você recupere metadados de dispositivos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização do dispositivo**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




