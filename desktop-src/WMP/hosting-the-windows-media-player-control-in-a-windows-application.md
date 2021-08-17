---
title: Hospedando o Windows Media Player controle em um Windows aplicativo
description: Hospedando o Windows Media Player controle em um Windows aplicativo
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, incorporando ActiveX controle
- Windows Media Player modelo de objeto, incorporando ActiveX controle
- modelo de objeto, incorporando ActiveX controle
- Windows Media Player Mobile, incorporando ActiveX controle
- Windows Media Player ActiveX controle,incorporação
- Windows Media Player Controle ActiveX dispositivo móvel, incorporação
- ActiveX controle,incorporação
- Windows Media Player,Windows baseados em Windows
- Windows Media Player modelo de objeto, Windows programas baseados em dados
- modelo de objeto, Windows com base em programas baseados em
- Windows Media Player Programas Windows baseados em dispositivos móveis
- Windows Media Player ActiveX controle,Windows programas baseados em Windows
- Windows Media Player Controle ActiveX dispositivos móveis,Windows baseados em Windows aplicativo
- ActiveX controle,Windows programas baseados em Windows
- incorporação Windows programa baseado em Windows
- incorporação,Windows baseados em programas baseados em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3c2b4d84194376bd16842f0a9567c83fce2aa616ed4bfef4f20f7255068e8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748273"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hospedando o Windows Media Player controle em um Windows aplicativo

Para usar o Windows Media Player ActiveX (incluindo a interface do usuário) em um programa baseado em Windows, você deve fornecer um contêiner ActiveX controle. A ATL fornece a **classe CAxWindow** para fornecer ActiveX de janela do host.

Para hospedar o Windows Media Player usando a **classe CAxWindow,** siga estas etapas:

1.  Inclua os seguintes headers:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Declare variáveis de membro, da seguinte forma:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Quando a janela do aplicativo for criada, chame **AtlAxWinInit**, que é necessário ao usar a janela ActiveX host da ATL.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Declare variáveis locais para códigos de retorno e para conter o ponteiro para a interface da janela do host:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Crie a janela do host:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Recuperar o ponteiro da interface da janela do host:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Crie o Windows Media Player na janela do host usando a ID da classe:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recupere o ponteiro da interface **IWMPPlayer:**
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Ao escrever seu próprio código, verifique se há erros em cada código de retorno **HRESULT.**

Para ver um exemplo completo que ilustra como hospedar o controle Windows Media Player ActiveX usando a **classe CAxWindow,** consulte o exemplo WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hospedando o Windows Media Player 10 Mobile no Windows CE

O Microsoft eMbedded Visual C++ 4.0 e o SDK do Pocket PC 2003 ou o SDK do Smartphone 2003 devem ser instalados ao desenvolver aplicativos baseados em Windows CE que hospedam um controle móvel do Windows Media Player 10. Além disso, ao contrário da ATL para Windows, a ATL para Windows CE não dá suporte ao modelo de threading de apartment. Portanto, você deve encontrar todas as instâncias de threading de apartment em seu projeto da ATL e alterá-las para usar threading livre.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Usando o Windows Media Player controle em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




