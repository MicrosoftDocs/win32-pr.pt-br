---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Instalação e configuração do provedor de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d420e9322d1d39816cdb9b3812b23b1e7e72e945c3d0f2ef95e7edff77f12276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121366"
---
# <a name="namespace-provider-configuration-and-installation"></a>Instalação e configuração do provedor de namespace

-   [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**WSCWriteNameSpaceOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Conforme mencionado anteriormente, o aplicativo de instalação para um provedor de namespace deve chamar [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) ou [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) para se registrar com o Ws232.dll e fornecer informações de configuração \_ estática. Para instalar no catálogo de 32 bits em uma plataforma de 64 bits, o provedor de namespace deve chamar [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) ou [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32). O Ws232.dll usa essas informações para realizar sua função de roteamento e em sua implementação \_ [**de WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) e [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). A [**função WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) é usada para remover um provedor de namespace do Registro e a [**função WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) é usada para alternar um provedor entre os estados ativo e inativo.

Em uma plataforma de 64 bits, [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) são funções semelhantes para lidar com o catálogo de 32 bits.

Os resultados dessas três operações não são visíveis para aplicativos que estão atualmente carregados e em execução. Somente os aplicativos que começam a ser executados após essas operações ocorrerem serão afetados por eles.

Essa arquitetura dá suporte explicitamente à instaláciação de vários provedores de namespace em uma única DLL, no entanto, cada provedor deve ter um GUID (identificador de provedor de namespace) exclusivo alocado e uma chamada separada para [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) ou [**WSCInstallNameSpaceEx deve**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) ocorrer para cada instanência (em plataformas de 64 bits, as funções do catálogo de 32 bits são [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) e [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)). Esse provedor pode determinar qual instanação está sendo invocada porque o identificador NSP (provedor de namespace) aparece como um parâmetro em cada função NSP.

 

 



