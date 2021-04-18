---
description: Demonstra o uso de funções básicas de gerenciamento de rede sem fio.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemplo de API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760234"
---
# <a name="native-wifi-api-sample"></a>Exemplo de API WiFi nativa

Um exemplo de API WiFi nativo que demonstra o uso de funções básicas de gerenciamento de rede sem fio está incluído no SDK (Software Development Kit) do Microsoft Windows. A versão mais recente do SDK do Windows está disponível no [centro de download](https://developer.microsoft.com/windows/downloads).

Por padrão, o código-fonte de exemplo WiFi nativo é instalado no seguinte diretório:

**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ amostras \\ NetDs \\ WLAN**

O exemplo de API WiFi nativo está localizado na seguinte pasta:

**AutoConfig**

O exemplo de WiFi nativo pode ser compilado e executado no Windows Vista e posterior, no Windows XP com Service Pack 3 (SP3) e na API de LAN sem fio para Windows XP com Service Pack 2 (SP2). Alguns recursos do exemplo não têm suporte no Windows XP com SP3 e na API de LAN sem fio para Windows XP com SP2. Para obter uma lista das funções com suporte pelo Windows XP com SP3 e pela API de LAN sem fio para Windows XP com SP2, consulte [suporte nativo à API WiFi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

O exemplo de WiFi nativo demonstra como executar as seguintes tarefas:

-   Enumere as interfaces sem fio. Consulte [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtenha os recursos de uma interface. Consulte [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2: * * não há suporte para esse recurso.

-   Consultar uma interface. Consulte [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Definir parâmetros para uma interface de rede. Consulte [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Essa função pode ser usada para ativar e desativar o rádio sem fio (e, portanto, habilitar ou desabilitar a conectividade de rede sem fio).
-   Verificar se há redes sem fio disponíveis. Consulte [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Obtenha a lista de redes sem fio disponíveis ou visíveis. Consulte [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Obter, salvar ou excluir um perfil. Consulte [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Conecte-se ou desconecte-se de uma rede sem fio. Consulte [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando WiFi nativo](using-native-wifi.md)
</dt> <dt>

[Fórum do SDK sem fio do Windows Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Solução de problemas de conexões sem fio do Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
