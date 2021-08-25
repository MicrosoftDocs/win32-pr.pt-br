---
description: Demonstra o uso de funções básicas de gerenciamento de rede sem fio.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Exemplo de API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801056"
---
# <a name="native-wifi-api-sample"></a>Exemplo de API WiFi nativa

um exemplo de API Wifi nativo que demonstra o uso de funções básicas de gerenciamento de rede sem fio está incluído no SDK (Software Development Kit) do Microsoft Windows. a versão mais recente do SDK do Windows está disponível no [centro de Download](https://developer.microsoft.com/windows/downloads).

Por padrão, o código-fonte de exemplo WiFi nativo é instalado no seguinte diretório:

**C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ amostras \\ NetDs \\ Wlan**

O exemplo de API WiFi nativo está localizado na seguinte pasta:

**AutoConfig**

o exemplo de Wifi nativo pode ser compilado e executado no Windows Vista e posterior, Windows xp com service pack 3 (SP3) e API de LAN sem fio para Windows XP com service pack 2 (SP2). alguns recursos do exemplo não têm suporte no Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2. para obter uma lista das funções com suporte pelo Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2, consulte [suporte nativo à api Wifi no Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

O exemplo de WiFi nativo demonstra como executar as seguintes tarefas:

-   Enumere as interfaces sem fio. Consulte [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtenha os recursos de uma interface. Consulte [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows xp com SP3 e API de LAN sem fio para Windows XP com SP2: * * não há suporte para esse recurso.

-   Consultar uma interface. Consulte [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Definir parâmetros para uma interface de rede. Consulte [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Essa função pode ser usada para ativar e desativar o rádio sem fio (e, portanto, habilitar ou desabilitar a conectividade de rede sem fio).
-   Verificar se há redes sem fio disponíveis. Consulte [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Obtenha a lista de redes sem fio disponíveis ou visíveis. Consulte [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Obter, salvar ou excluir um perfil. Consulte [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)e [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Conexão ou desconectar-se de uma rede sem fio. Consulte [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) e [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando WiFi nativo](using-native-wifi.md)
</dt> <dt>

[Windows Fórum do SDK sem fio do vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[solução de problemas de conexões sem fio Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
