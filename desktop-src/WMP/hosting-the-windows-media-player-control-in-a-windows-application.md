---
title: Hospedando o controle do Windows Media Player em um aplicativo do Windows
description: Hospedando o controle do Windows Media Player em um aplicativo do Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, programas baseados no Windows
- Modelo de objeto do Windows Media Player, programas baseados no Windows
- modelo de objeto, programas baseados no Windows
- Windows Media Player Mobile, programas baseados no Windows
- Controle ActiveX do Windows Media Player, programas baseados no Windows
- Controle ActiveX móvel do Windows Media Player, programas baseados no Windows
- Controle ActiveX, programas baseados no Windows
- Incorporação de programas baseados no Windows
- incorporação, programas baseados no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292552"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hospedando o controle do Windows Media Player em um aplicativo do Windows

Para usar o controle ActiveX do Windows Media Player (incluindo a interface do usuário) em um programa baseado no Windows, você deve fornecer um contêiner de controle ActiveX. A ATL fornece a classe **CAxWindow** para fornecer a funcionalidade de janela do host do ActiveX.

Para hospedar o controle do Windows Media Player usando a classe **CAxWindow** , siga estas etapas:

1.  Inclua os seguintes cabeçalhos:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Declare variáveis de membro, da seguinte maneira:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Quando a janela do aplicativo for criada, chame **AtlAxWinInit**, que é necessário ao usar a janela host ActiveX do ATL.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Declare variáveis locais para códigos de retorno e que contenham o ponteiro para a interface de janela do host:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Crie a janela do host:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Recupere o ponteiro de interface de janela do host:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Crie o controle do Windows Media Player na janela do host usando a ID da classe:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recupere o ponteiro de interface **IWMPPlayer** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Ao escrever seu próprio código, certifique-se de verificar se há erros em cada código de retorno de **HRESULT** .

Para obter um exemplo completo que ilustra como hospedar o controle ActiveX do Windows Media Player usando a classe **CAxWindow** , consulte o exemplo WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hospedando o controle móvel do Windows Media Player 10 no Windows CE

O Microsoft eMbedded Visual C++ 4,0 e o SDK do Pocket PC 2003 ou o SDK do Smartphone 2003 devem ser instalados durante o desenvolvimento de aplicativos baseados em Windows CE que hospedam um controle móvel do Windows Media Player 10. Além disso, diferentemente do ATL para Windows, a ATL para Windows CE não oferece suporte ao modelo de Threading Apartment. Portanto, você deve encontrar todas as instâncias de threading de apartamento em seu projeto ATL e alterá-las para usar Threading gratuito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




