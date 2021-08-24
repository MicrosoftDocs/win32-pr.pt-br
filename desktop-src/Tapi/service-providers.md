---
description: Os provedores de serviços implementam controles detalhados de dispositivo de telefonia. Um provedor de serviços de telefonia (TSP) fornece controles de chamada e um provedor de serviços de mídia, se ele existir, fornece controle sobre o fluxo de mídia.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0bc427b79daadc8dc89e49a29e18ebbd9797bed74da7f890dc851d6ee97b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773116"
---
# <a name="service-providers"></a>Provedores de serviço

Os provedores de serviços implementam controles detalhados de dispositivo de telefonia. Um provedor de serviços de telefonia (TSP) fornece controles de chamada e um provedor de serviços de mídia, se ele existir, fornece controle sobre o fluxo de mídia.

Todos os provedores de serviços de telefonia são executados no processo TAPISRV. Os provedores de serviços podem criar threads no contexto TAPISRV conforme necessário para fazer seu trabalho e ter certeza de que nenhum dos recursos que eles criam será destruído pela saída de qualquer aplicativo individual. O servidor TAPI converte comandos de aplicativo conforme necessário em um conjunto consistente de comandos conhecidos como TSPI (Interface do Provedor de Serviços de Telefonia).

Os provedores de serviços de mídia são executados no espaço de processo do aplicativo, permitindo a resposta rápida às vezes necessária nos controles de mídia. A DLL do TAPI fornece uma adesão consistente à MSPI (Interface do Provedor de Serviços de Mídia).

Para obter uma cobertura mais detalhada dos provedores de serviços, consulte Visão [geral do provedor de serviços TAPI.](./tapi-service-provider-overview.md)

Sob a DLL do provedor de serviços de telefonia, o provedor de serviços pode usar qualquer função do sistema ou outros componentes necessários. Essas funções incluem [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**DeviceIoControl,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)que funcionam com componentes e serviços de modo kernel independentes projetados pelo fornecedor de hardware, bem como dispositivos padrão, como portas seriais e paralelas, para controlar dispositivos externos anexados localmente. Eles também podem acessar serviços de rede (como RPC, Windows Soquetes e Pipes Nomeados) para telefonia de cliente/servidor.

A DLL da interface do usuário do provedor de serviços de telefonia é carregada pela TAPI no processo de um aplicativo que invoca qualquer uma das funções do provedor de serviços que pode exibir uma caixa de diálogo (por exemplo, [**linha TSPIConfigDialog \_**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). O provedor de serviços também pode fazer com que sua DLL de interface do usuário associada seja carregada e executada no processo de um aplicativo se o provedor de serviços precisar exibir a interface do usuário em momentos inesperados, como para exibir a caixa de diálogo **Talk/Hang-up** exibida pelo UNIMODEM (Driver Universal do Modem) quando um modem de dados é usado para discar uma chamada de voz interativa usando a linha [**TSPIMakeCall \_**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (normalmente não considerada uma função de geração de interface do usuário).

O manipulador de solicitação de proxy é um aplicativo de telefonia completo que normalmente é executado em um servidor de telefonia (o mesmo servidor no qual o provedor de serviços de telefonia está sendo executado para os dispositivos de linha associados). Essa arquitetura, em vez da arquitetura do provedor de serviços WOSA, é usada quando um serviço específico é implementado mais adequadamente em um aplicativo do que em um driver no servidor. Por exemplo, as funções de gerenciamento do AGENTE ACD são implementadas em um manipulador de solicitação de proxy em vez de em um provedor de serviços.

O provedor de serviço de driver UNIMODEM para controle de modem está disponível em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 e Windows NT. Windows A telefonia também inclui um mapeado TSPI (Interface de Provedor de Serviços de Telefonia) no modo kernel genérico, KMDDSP, que permite que os provedores de serviços sejam implementados como drivers de dispositivo no modo kernel.

 

 
