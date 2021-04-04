---
description: Os provedores de serviço implementam controles de dispositivo de telefonia detalhados. Um provedor de serviços de telefonia (TSP) fornece controles de chamada e um provedor de serviços de mídia, se existir, fornece controle sobre o fluxo de mídia.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424c11d5b99af7440835e8822a5631e1b36f48cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922974"
---
# <a name="service-providers"></a>Provedores de serviço

Os provedores de serviço implementam controles de dispositivo de telefonia detalhados. Um provedor de serviços de telefonia (TSP) fornece controles de chamada e um provedor de serviços de mídia, se existir, fornece controle sobre o fluxo de mídia.

Todos os provedores de serviço de telefonia são executados no processo TAPISRV. Os provedores de serviços podem criar threads no contexto de TAPISRV conforme necessário para realizar seu trabalho e ter certeza de que nenhum dos recursos que eles criam será destruído pela saída de qualquer aplicativo individual. O servidor TAPI traduz comandos de aplicativo conforme necessário em um conjunto consistente de comandos conhecidos como TSPI (interface de provedor de serviços de telefonia).

Os provedores de serviço de mídia são executados no espaço de processo do aplicativo, permitindo a resposta rápida às vezes necessária nos controles de mídia. A DLL TAPI fornece a adesão consistente à MSPI (interface do provedor de serviços de mídia).

Para obter uma cobertura mais detalhada dos provedores de serviço, consulte [visão geral do provedor de serviços TAPI](./tapi-service-provider-overview.md).

Sob a DLL do provedor de serviços de telefonia, o provedor de serviços pode usar qualquer função do sistema ou outros componentes necessários. Essas funções incluem [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol), que trabalham com componentes e serviços de modo kernel independentes de hardware independente, bem como dispositivos padrão, como portas seriais e paralelas para controlar dispositivos externos e anexados localmente. Eles também podem acessar os serviços de rede (como RPC, Windows Sockets e pipes nomeados) para a telefonia do cliente/servidor.

A DLL da interface do usuário do provedor de serviços de telefonia é carregada pela TAPI no processo de um aplicativo que invoca qualquer uma das funções de provedor de serviço que podem exibir uma caixa de diálogo (por exemplo, [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)). O provedor de serviços também pode fazer com que sua DLL de interface do usuário associada seja carregada e executada no processo de um aplicativo se o provedor de serviços precisar exibir a interface do usuário em momentos inesperados, por exemplo, para exibir a caixa de diálogo de **fala/desligamento** exibida pelo Universal Modem Driver (uniatendimentor) quando um modem de dados é usado para discar uma chamada de voz interativa usando [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (normalmente não é considerado uma função que gera uma interface do usuário).

O manipulador de solicitação de proxy é um aplicativo de telefonia completo que normalmente é executado em um servidor de telefonia (o mesmo servidor no qual o provedor de serviços de telefonia está sendo executado para os dispositivos de linha associados). Essa arquitetura, em vez da arquitetura do provedor de serviços do WOSA, é usada quando um serviço específico é implementado mais adequadamente em um aplicativo do que em um driver no servidor. Por exemplo, as funções de gerenciamento de agente ad são implementadas em um manipulador de solicitação de proxy em vez de em um provedor de serviços.

O provedor de serviços de driver Unimodem para o controle de modem está disponível em sistemas operacionais Windows Server 2003, Windows XP, Windows 2000 e Windows NT. A telefonia do Windows também inclui um mapeador de TSPI (interface do provedor de serviços de telefonia) de modo kernel genérico, KMDDSP, que permite que os provedores de serviços sejam implementados como drivers de dispositivo no modo kernel.

 

 
