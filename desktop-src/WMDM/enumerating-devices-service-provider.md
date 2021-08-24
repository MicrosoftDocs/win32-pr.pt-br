---
title: Enumerando dispositivos (WMDM)
description: Windows A Gerenciador de Dispositivos de mídia mantém um cache de dispositivos conectados. Saiba como Windows Mídia Gerenciador de Dispositivos mantém ou atualiza seu cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Mídia Gerenciador de Dispositivos, enumerando dispositivos
- Gerenciador de Dispositivos,enumerando dispositivos
- guia de programação, enumeração de dispositivos
- provedores de serviços, enumerando dispositivos
- criando provedores de serviços, enumerando dispositivos
- enumerando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767046"
---
# <a name="enumerating-devices-wmdm"></a>Enumerando dispositivos (WMDM)

Windows O Gerenciador de Dispositivos de mídia mantém um cache de dispositivos conectados que é atualizado quando um aplicativo Windows Media Gerenciador de Dispositivos é iniciado, quando um dispositivo Plug and Play (PnP) se conecta ou desconecta ou quando o aplicativo chama [**IWMDeviceManager2::Reinicializar**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Esse cache é exposto ao aplicativo quando chama [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) ou [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2). Cada dispositivo é exposto ao aplicativo como uma interface [**IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) Se o provedor de serviços estiver registrado para lidar com dispositivos PnP, Windows mídia Gerenciador de Dispositivos estará ciente da lista atual de dispositivos conectados. Se o provedor de serviços estiver registrado para lidar com dispositivos não PnP, o provedor de serviços será responsável por descobrir dispositivos anexados. Um provedor de serviços só pode ser registrado para dispositivos PnP ou não PnP, nunca ambos.

As ações a seguir mostram como Windows Media Gerenciador de Dispositivos mantém ou atualiza seu cache. Observe que o cache nunca é atualizado quando um dispositivo não PnP se conecta ou se desconecta.

Um Windows de Gerenciador de Dispositivos mídia é iniciado

-   Windows A Gerenciador de Dispositivos de mídia recupera uma lista de dispositivos PnP anexados do subsistema PnP e chama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) no SP registrado para cada dispositivo conectado. (Ele descobre o provedor de serviços correto consultando o parâmetro de dispositivo WMDMSPCLSID para a ID de classe do provedor de serviços responsável por esse dispositivo. Consulte [Parâmetros de dispositivo para](device-parameters.md) obter mais informações.) Todos os dispositivos retornados são adicionados ao Windows mídia Gerenciador de Dispositivos cache de dispositivos.
-   Windows O Gerenciador de Dispositivos de mídia localiza todos os provedores de serviços não PnP registrados com ele e chama [**IMDServiceProvider::EnumDevices em**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) cada provedor de serviços para obter uma lista de dispositivos de cada um. Todos os dispositivos retornados são adicionados ao cache.

O aplicativo chama IWMDeviceManager/2::EnumDevices/2

-   Windows A Gerenciador de Dispositivos de mídia retorna sua lista de dispositivos armazenados em cache.

Um dispositivo PnP se conecta

-   Windows A Gerenciador de Dispositivos de mídia localiza o provedor de serviços relevante e chama **IMDServiceProvider2::CreateDevice** e adiciona o dispositivo ao cache.
-   Se o aplicativo implementar [**IWMDMNotification,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)o Windows Media Gerenciador de Dispositivos [**chamará IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) com uma notificação de chegada.

Um dispositivo PnP se desconecta

-   Windows A Gerenciador de Dispositivos de mídia remove o item de seu cache.
-   Se o aplicativo implementar IWMDMNotification, o Windows Media Gerenciador de Dispositivos chamarÁ IWMDMNotification::WMDMMessage com uma notificação de partida.

O aplicativo chama IWMDeviceManager2::Reinitialize

-   Atualiza o cache com todos os dispositivos conectados.

Um dispositivo não PnP se conecta ou desconecta

-   Windows A Gerenciador de Dispositivos mídia não é informada sobre a chegada ou partida e não toma nenhuma ação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um provedor de serviços**](creating-a-service-provider.md)
</dt> </dl>

 

 




