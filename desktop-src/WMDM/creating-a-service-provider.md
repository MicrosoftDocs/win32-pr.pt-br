---
title: Criando um provedor de serviços
description: Criando um provedor de serviços
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Gerenciador de Dispositivos de mídia, criando provedores de serviços
- Gerenciador de Dispositivos, criando provedores de serviços
- Windows Gerenciador de Dispositivos de mídia, guia de programação
- Gerenciador de Dispositivos, guia de programação
- Guia de programação, provedores de serviços
- guia de programação, Windows de mídia Gerenciador de Dispositivos
- Guia de programação, criando provedores de serviços
- Windows Gerenciador de Dispositivos de mídia, provedores de serviço
- Gerenciador de Dispositivos, provedores de serviços
- provedores de serviços, criando
- criando provedores de serviços, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f5b6abfba6b143e0a8ab7913ed1c1f53bbdeb3104a6a8450e438843349598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585849"
---
# <a name="creating-a-service-provider"></a>Criando um provedor de serviços

Um provedor de serviços é um componente que serve como um meio entre um aplicativo e um dispositivo. Windows A mídia Gerenciador de Dispositivos roteia solicitações do aplicativo para o provedor de serviços, que é então responsável pela comunicação com o dispositivo ou pela execução da ação solicitada. Um provedor de serviços geralmente se comunica com um driver para habilitar a comunicação com o dispositivo. um provedor de serviços é um componente COM que implementa as interfaces chamadas por Windows Gerenciador de Dispositivos de mídia. A interface raiz do objeto do provedor de serviços é [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). depois de obter essa interface, Windows mídia Gerenciador de Dispositivos pode obter outras interfaces por meio da implementação do provedor de serviços de vários métodos. As interfaces que um provedor de serviços deve implementar estão listadas em [interfaces obrigatórias e opcionais](mandatory-and-optional-interfaces.md). A hierarquia de interfaces é mostrada em [interfaces para provedores de serviços](interfaces-for-service-providers.md).

> [!Note]  
> Você não deve tentar criar um provedor de serviços MTP; em vez disso, você deve usar o provedor de serviços MTP e os drivers fornecidos pela Microsoft.

 

Antes de tentar criar um provedor de serviços, você deve compreender totalmente as chamadas que um aplicativo fará em um provedor de serviços. leia [criando um aplicativo de Gerenciador de Dispositivos de mídia Windows](creating-a-windows-media-device-manager-application.md) para obter uma ideia das tarefas básicas e chamadas que um aplicativo fará em um provedor de serviços quando ele estiver tentando se comunicar com um dispositivo.

A lista a seguir mostra as principais etapas do desenvolvimento de um provedor de serviços:

1.  Inclua (e, opcionalmente, compile) o cabeçalho e os arquivos de biblioteca necessários para seu projeto. Consulte [bibliotecas e cabeçalhos necessários para um provedor de serviços](required-libraries-and-headers-for-a-service-provider.md) para obter a lista de arquivos necessários.
2.  Implemente todas as outras interfaces de provedor de serviços necessárias ou opcionais (consulte [interfaces obrigatórias e opcionais](mandatory-and-optional-interfaces.md)). Normalmente, as interfaces serão chamadas nesta ordem:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Verifique se o seu provedor de serviços ou dispositivo instala as chaves de registro apropriadas durante a instalação. Essas chaves especificam os parâmetros do dispositivo, registram o provedor de serviços como um plug-in e habilitam notificações de Plug and Play para a chegada e a remoção do dispositivo. Consulte [parâmetros do dispositivo](device-parameters.md), [registrando o provedor de serviços](registering-the-service-provider.md)e [habilitando o PNP para dispositivos](enabling-pnp-for-devices.md).
4.  Na instanciação da sua classe, autentique o provedor de serviços no construtor. Para fazer isso, crie uma classe [CSecureChannelServer](csecurechannelserver-class.md) e defina o certificado. Implemente a interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) e chame os métodos da classe CSecureChannelServer instanciada anteriormente. Consulte [Autenticando o provedor de serviços](authenticating-the-service-provider.md) para saber como criar uma instância da classe CSecureChannelServer e implementar os métodos IComponentAuthenticate.
5.  Windows A mídia Gerenciador de Dispositivos consultará seu provedor de serviços para obter uma lista de dispositivos conectados chamando [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) ou [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), dependendo se o provedor de serviços lida com plug and Play dispositivos. O provedor de serviços deve retornar uma lista de objetos [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) que representam os dispositivos conectados. Consulte [enumerando dispositivos](enumerating-devices-service-provider.md) para obter mais detalhes.
6.  Antes de tratar qualquer chamada, verifique se um canal seguro foi estabelecido. Chame [**CSecureChannelServer:: fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) antes de executar qualquer ação. Se essa chamada falhar, retornar WMDM \_ E não \_ certificado.
7.  Você precisará de um par de certificados/chaves emitido pela Microsoft para poder lidar com materiais protegidos por DRM. Consulte [lidando com conteúdo protegido no provedor de serviços](handling-protected-content-in-the-service-provider.md) para obter mais informações.
8.  para permitir que seu dispositivo seja sincronizado automaticamente com o Windows Media Player, ele deve atender aos requisitos listados em [habilitando a sincronização com Windows Media Player](enabling-synchronization-with-windows-media-player.md).
9.  para permitir que o dispositivo apareça no Windows Explorer, você deve executar algumas etapas especiais, detalhadas em [requisitos para que players de áudio portáteis apareçam no Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 