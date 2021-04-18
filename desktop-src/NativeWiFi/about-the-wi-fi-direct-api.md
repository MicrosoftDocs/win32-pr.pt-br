---
description: A API Wi-Fi nativa contém um conjunto de funções que dão suporte ao uso de Wi-Fi direto para aplicativos de área de trabalho.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Sobre o recurso Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785407"
---
# <a name="about-the-wi-fi-direct-feature"></a>Sobre o recurso Wi-Fi Direct

A API Wi-Fi nativa contém um conjunto de funções que dão suporte ao uso de Wi-Fi direto para aplicativos de área de trabalho. A partir do Windows 8 e do Windows Server 2012, Wi-Fi funções diretas foram adicionadas à API WiFi nativa.

O recurso direto Wi-Fi é baseado no desenvolvimento do Wi-Fi especificação técnica ponto a ponto v 1.1 pela Aliança de Wi-Fi (consulte [especificações publicadas da Wi-Fi Alliance](https://www.wi-fi.org/)). O objetivo do Wi-Fi especificação técnica ponto a ponto é fornecer uma solução para Wi-Fi conectividade de dispositivo para dispositivo sem a necessidade de um ponto de acesso sem fio (AP sem fio) configurar a conexão ou o uso do mecanismo existente Wi-Fi ad hoc (IBSS).

> [!Note]  
> O modo ad hoc pode não estar disponível em versões futuras do Windows. A partir do Windows 8.1 e do Windows Server 2012 R2, use Wi-Fi Direct em vez disso.

 

Para um aplicativo de desktop, o recurso direto Wi-Fi requer que os dispositivos Wi-FI Direct sejam emparelhados anteriormente pelo usuário com a interface do usuário da experiência de emparelhamento do Windows. Após a conclusão desse emparelhamento, é armazenado um perfil que permite que as funções Wi-Fi diretas sejam usadas para iniciar uma sessão Wi-Fi Direct para estabelecer uma conexão entre os dispositivos Wi-Fi Direct.

As funções a seguir dão suporte ao recurso direto Wi-Fi.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -indica que o aplicativo deseja cancelar uma função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendente que não foi concluída.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -fecha um identificador para o serviço direto Wi-Fi.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -fecha uma sessão após uma chamada bem-sucedida anterior à função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -abre um identificador para o serviço Wi-Fi Direct e negocia uma versão da API Wi-Fi Direct a ser usada.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) – recupera e aplica um perfil armazenado para um Wi-Fi dispositivo herdado direto.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -inicia uma conexão sob demanda com um dispositivo específico Wi-Fi Direct, que foi anteriormente emparelhado por meio da experiência de emparelhamento do Windows.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) – atualiza a visibilidade do dispositivo para o endereço de dispositivo Wi-Fi direto para um determinado nó de dispositivo Wi-Fi Direct.
-   [**WFD \_ ABRIR \_ sessão \_ de \_ retorno de chamada concluído**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) – define a função de retorno de chamada que é chamado pela função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) quando a operação **WFDStartOpenSession** é concluída

Para obter mais informações sobre como usar Wi-Fi diretamente em um aplicativo de área de trabalho, consulte [usando o Wi-Fi funções diretas](using-the-wi-fi-direct-api.md).

Para obter mais informações sobre Wi-Fi Direct para uso em aplicativos da Windows Store, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e classes relacionadas no namespace [**Windows. Networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Outros recursos**
</dt> <dt>

[Sobre WiFi nativo](about-native-wifi.md)
</dt> <dt>

[Sobre a API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Sobre a API ad hoc sem fio](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Usando o Wi-Fi funções diretas](using-the-wi-fi-direct-api.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**\_retorno de \_ \_ chamada completo de sessão aberta WFD \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**{1&amp;gt;{2&amp;gt;Windows.Networking.Proximity&amp;lt;2}&amp;lt;1}**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
