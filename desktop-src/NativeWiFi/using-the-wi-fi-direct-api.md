---
description: Mostra como usar funções Wi-Fi Direct em aplicativos da área de trabalho.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Usando as funções Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9a00a5474632ed54a84a7dc8cc5c64774e7cfe7547e6994acee599df2461ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684726"
---
# <a name="using-the-wi-fi-direct-functions"></a>Usando as funções Wi-Fi Direct

Este tópico mostra como usar funções Wi-Fi Direct em aplicativos da área de trabalho. A partir Windows 8 e Windows Server 2012, Wi-Fi Funções Diretas foram adicionadas à API Wi-Fi Nativa.

O Wi-Fi Direct baseia-se no desenvolvimento da especificação técnica ponto a ponto do Wi-Fi v1.1 pela Wi-Fi Alliance (consulte [Especificações publicadas da Wi-Fi Alliance).](https://www.wi-fi.org/) A meta da especificação técnica ponto a ponto do Wi-Fi é fornecer uma solução para Wi-Fi conectividade entre dispositivos sem a necessidade de um ponto de acesso sem fio (AP sem fio) para configurar a conexão ou o uso do mecanismo Wi-Fi Ad hoc (IBSS) existente.

> [!Note]  
> O modo ad hoc pode não estar disponível em versões futuras do Windows. Começando com Windows 8.1 e Windows Server 2012 R2, use Wi-Fi Direct.

 

As funções a seguir suportam o recurso Wi-Fi Direct.

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) – indica que o aplicativo deseja cancelar uma função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendente que não foi concluída.
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) – fecha um handle para o Wi-Fi Direct.
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) – fecha uma sessão após uma chamada bem-sucedida anteriormente para a [**função WFDStartOpenSession.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) – abre um handle para o serviço Wi-Fi Direct e negocia uma versão da API Direta de Wi-FI a ser usada.
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) – recupera e aplica um perfil armazenado para um Wi-Fi herdado direto.
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) – inicia uma conexão sob demanda para um dispositivo Wi-Fi Direct específico, que foi emparelhado anteriormente por meio da experiência de Windows emparelhamento.
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) – atualiza a visibilidade do dispositivo para o endereço do dispositivo Wi-Fi Direct para um determinado nó de dispositivo Wi-Fi Direct.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) – define a função de retorno de chamada que é chamada pela função [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) quando a **operação WFDStartOpenSession** é concluída

Para um aplicativo da área de trabalho, o recurso Wi-Fi Direct exige que os dispositivos Wi-FI Direct sejam emparelhados anteriormente pelo usuário com a interface do usuário Windows experiência de emparelhamento. Depois que esse emparelhamento é concluído, um perfil é armazenado que permite que as funções Wi-Fi Direct sejam usadas para iniciar uma sessão do Wi-Fi Direct para estabelecer uma conexão entre os dispositivos Wi-Fi Direct.

Para usar o Wi-Fi Direct, um aplicativo deve primeiro obter um alçado para o serviço Wi-Fi Direct chamando a [**função WFDOpenHandle.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) O Wi-Fi do WFD (Direct) retornado pela função **WFDOpenHandle** é usado para chamadas de função Wi-Fi Direct subsequentes feitas ao serviço Wi-Fi Direct.

A [**função WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia uma operação assíncrona para iniciar uma conexão sob demanda com um dispositivo Wi-Fi Direct específico. O dispositivo Wi-Fi destino deve ter sido emparelhado anteriormente por meio da experiência Windows emparelhamento. Quando a operação assíncrona for concluída, a função de retorno de chamada especificada no *parâmetro pfnCallback* será chamada.

Depois que um aplicativo for feito usando o serviço Wi-Fi Direct, o aplicativo deverá chamar a função [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) para sinalizar ao serviço Wi-Fi Direct que o aplicativo é feito usando o serviço. Isso permite que o Wi-Fi Direct libere recursos usados pelo aplicativo.

Para obter mais informações sobre o Wi-Fi Direct para uso em aplicativos da Windows Store, consulte [**Peer Ltda**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) e classes relacionadas no [**Windows. Namespace Networking.Proximity.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Outros recursos**
</dt> <dt>

[Sobre Wifi nativo](about-native-wifi.md)
</dt> <dt>

[Sobre a API wi-fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Sobre o recurso Wi-Fi Direct](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**Peer Ltda**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**RETORNO DE CHAMADA COMPLETO DA SESSÃO ABERTA \_ \_ \_ \_ DO WFD**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
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

 

 
