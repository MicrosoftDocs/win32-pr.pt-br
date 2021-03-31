---
title: Enumerando dispositivos (WMDM)
description: Enumerando dispositivos
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Gerenciador de Dispositivos, enumerando dispositivos
- Gerenciador de Dispositivos, enumerando dispositivos
- Guia de programação, enumerando dispositivos
- provedores de serviços, enumerando dispositivos
- criando provedores de serviços, enumerando dispositivos
- Enumerando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638919"
---
# <a name="enumerating-devices-wmdm"></a>Enumerando dispositivos (WMDM)

O Windows Media Gerenciador de Dispositivos mantém um cache de dispositivos conectados que são atualizados quando um aplicativo do Windows Media Gerenciador de Dispositivos é iniciado, quando um dispositivo Plug and Play (PnP) se conecta ou se desconecta, ou quando o aplicativo chama [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Esse cache é exposto ao aplicativo quando chama [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) ou [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Cada dispositivo é exposto ao aplicativo como uma interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) . Se o provedor de serviços estiver registrado para lidar com dispositivos PnP, o Windows Media Gerenciador de Dispositivos estará ciente da lista atual de dispositivos conectados. Se o provedor de serviços estiver registrado para lidar com dispositivos não PnP, o provedor de serviços será responsável por descobrir os dispositivos anexados. Um provedor de serviços só pode ser registrado para dispositivos PnP ou não PnP, nunca ambos.

As ações a seguir mostram como o Windows Media Gerenciador de Dispositivos mantém ou atualiza seu cache. Observe que o cache nunca é atualizado quando um dispositivo não PnP se conecta ou se desconecta.

Um aplicativo do Windows Media Gerenciador de Dispositivos é iniciado

-   O Windows Media Gerenciador de Dispositivos Recupera uma lista de dispositivos PnP anexados do subsistema PnP e chama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) no SP registrado para cada dispositivo conectado. (Ele descobre o provedor de serviços correto consultando o parâmetro de dispositivo WMDMSPCLSID para a ID de classe do provedor de serviços responsável por este dispositivo. Consulte [parâmetros do dispositivo](device-parameters.md) para obter mais informações.) Todos os dispositivos retornados são adicionados ao cache do Windows Media Gerenciador de Dispositivos de dispositivos.
-   O Windows Media Gerenciador de Dispositivos localiza todos os provedores de serviço não PnP registrados com ele e chama [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) em cada provedor de serviços para obter uma lista de dispositivos de cada um. Todos os dispositivos retornados são adicionados ao cache.

O aplicativo chama IWMDeviceManager/2:: EnumDevices/2

-   O Windows Media Gerenciador de Dispositivos retorna sua lista de dispositivos armazenados em cache.

Um dispositivo PnP se conecta

-   O Windows Media Gerenciador de Dispositivos localiza o provedor de serviços relevante e chama **IMDServiceProvider2:: CreateDevice** e adiciona o dispositivo ao seu cache.
-   Se o aplicativo implementar [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), o Windows Media Gerenciador de dispositivos chamará [**IWMDMNotification:: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) com uma notificação de chegada.

Um dispositivo PnP se desconecta

-   O Windows Media Gerenciador de Dispositivos remove o item do cache.
-   Se o aplicativo implementar IWMDMNotification, o Windows Media Gerenciador de Dispositivos chamará IWMDMNotification:: WMDMMessage com uma notificação de saída.

O aplicativo chama IWMDeviceManager2:: Reinitialize

-   Atualiza o cache com todos os dispositivos conectados.

Um dispositivo não PnP se conecta ou desconecta

-   O Windows Media Gerenciador de Dispositivos não é informado sobre a chegada ou a partida e não executa nenhuma ação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 




