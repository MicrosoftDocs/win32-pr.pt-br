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
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="cb7b3-119">Hospedando o controle do Windows Media Player em um aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="cb7b3-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="cb7b3-120">Para usar o controle ActiveX do Windows Media Player (incluindo a interface do usuário) em um programa baseado no Windows, você deve fornecer um contêiner de controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="cb7b3-121">A ATL fornece a classe **CAxWindow** para fornecer a funcionalidade de janela do host do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="cb7b3-122">Para hospedar o controle do Windows Media Player usando a classe **CAxWindow** , siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="cb7b3-123">Inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="cb7b3-124">Declare variáveis de membro, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="cb7b3-125">Quando a janela do aplicativo for criada, chame **AtlAxWinInit**, que é necessário ao usar a janela host ActiveX do ATL.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="cb7b3-126">Declare variáveis locais para códigos de retorno e que contenham o ponteiro para a interface de janela do host:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="cb7b3-127">Crie a janela do host:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="cb7b3-128">Recupere o ponteiro de interface de janela do host:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="cb7b3-129">Crie o controle do Windows Media Player na janela do host usando a ID da classe:</span><span class="sxs-lookup"><span data-stu-id="cb7b3-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="cb7b3-130">Recupere o ponteiro de interface **IWMPPlayer** :</span><span class="sxs-lookup"><span data-stu-id="cb7b3-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="cb7b3-131">Ao escrever seu próprio código, certifique-se de verificar se há erros em cada código de retorno de **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cb7b3-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="cb7b3-132">Para obter um exemplo completo que ilustra como hospedar o controle ActiveX do Windows Media Player usando a classe **CAxWindow** , consulte o exemplo WMPHost.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="cb7b3-133">Hospedando o controle móvel do Windows Media Player 10 no Windows CE</span><span class="sxs-lookup"><span data-stu-id="cb7b3-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="cb7b3-134">O Microsoft eMbedded Visual C++ 4,0 e o SDK do Pocket PC 2003 ou o SDK do Smartphone 2003 devem ser instalados durante o desenvolvimento de aplicativos baseados em Windows CE que hospedam um controle móvel do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="cb7b3-135">Além disso, diferentemente do ATL para Windows, a ATL para Windows CE não oferece suporte ao modelo de Threading Apartment.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="cb7b3-136">Portanto, você deve encontrar todas as instâncias de threading de apartamento em seu projeto ATL e alterá-las para usar Threading gratuito.</span><span class="sxs-lookup"><span data-stu-id="cb7b3-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb7b3-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb7b3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb7b3-138">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="cb7b3-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="cb7b3-139">**Usando o controle do Windows Media Player em um programa C++**</span><span class="sxs-lookup"><span data-stu-id="cb7b3-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




