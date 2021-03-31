---
title: Usando capas com o controle do Windows Media Player
description: Usando capas com o controle do Windows Media Player
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, C++
- Modelo de objeto do Windows Media Player, C++
- modelo de objeto, C++
- Windows Media Player Mobile, C++
- Controle ActiveX do Windows Media Player, C++
- Controle ActiveX móvel do Windows Media Player, C++
- Controle ActiveX, C++
- Incorporação de programa C++
- incorporando, programas em C++
- Controle ActiveX do Windows Media Player, capas
- Controle ActiveX móvel do Windows Media Player, capas
- Controle ActiveX, capas
- capas, incorporando controle ActiveX
- Capas do Windows Media Player, incorporando controle ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159850"
---
# <a name="using-skins-with-the-windows-media-player-control"></a><span data-ttu-id="7ff5b-124">Usando capas com o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="7ff5b-124">Using Skins with the Windows Media Player Control</span></span>

<span data-ttu-id="7ff5b-125">Ao inserir o controle do Windows Media Player em um programa C++, você pode personalizar a interface do usuário do Player aplicando um arquivo de definição de capa a ele.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-125">When you embed the Windows Media Player control in a C++ program, you can customize the Player user interface (UI) by applying a skin definition file to it.</span></span> <span data-ttu-id="7ff5b-126">Um arquivo de definição de capa é um documento baseado em XML que especifica o layout de componentes de interface do usuário padrão e personalizáveis e quaisquer elementos gráficos que o acompanham.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-126">A skin definition file is an XML-based document specifying the layout of standard and customizable UI components and any accompanying graphics.</span></span> <span data-ttu-id="7ff5b-127">Usando o Microsoft JScript, você pode especificar o comportamento desses componentes e manipular o controle do Windows Media Player sem a sobrecarga da sintaxe de C++ e COM.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-127">Using Microsoft JScript, you can specify the behavior of these components and manipulate the Windows Media Player control without the overhead of C++ and COM syntax.</span></span>

<span data-ttu-id="7ff5b-128">As capas fornecem uma maneira fácil de manter o código de interface do usuário e o código do programa principal separados para que possam ser mantidos e desenvolvidos de forma independente.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-128">Skins provide an easy way to keep your user interface code and your main program code separate so that they can be maintained and developed independently.</span></span> <span data-ttu-id="7ff5b-129">Você também pode reutilizar as capas originalmente projetadas para uso pelo Player autônomo no modo de capa.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-129">You can also reuse skins originally designed for use by the standalone Player in skin mode.</span></span> <span data-ttu-id="7ff5b-130">O código de capa que você cria especificamente para programas C++ pode interagir com seus programas por meio de um objeto programável que seu programa pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-130">Skin code that you design specifically for C++ programs can interact with your programs through a scriptable object that your program can provide.</span></span>

<span data-ttu-id="7ff5b-131">Para habilitar o modo de capa para o controle do Windows Media Player, o programa deve implementar a interface **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="7ff5b-131">To enable skin mode for the Windows Media Player control, your program must implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="7ff5b-132">Embora você possa usar as capas com o controle e o controle remoto ao mesmo tempo, você pode usar essa interface para habilitar qualquer recurso sem habilitar o outro.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-132">Although you can use skins with the control and remote the control at the same time, you can use this interface to enable either feature without enabling the other.</span></span> <span data-ttu-id="7ff5b-133">Para desabilitar a comunicação remota, basta passar um valor de "local" como o parâmetro out do método **Getservicetype** e retornar um HRESULT de E \_ NOTIMPL do método **getApplicationName** .</span><span class="sxs-lookup"><span data-stu-id="7ff5b-133">To disable remoting, simply pass a value of "Local" as the out parameter of the **GetServiceType** method, and return an HRESULT of E\_NOTIMPL from the **GetApplicationName** method.</span></span>

<span data-ttu-id="7ff5b-134">Para alternar o controle do Windows Media Player para o modo de capa, chame o método **IWMPPlayer::p UT \_ UIMODE** , passando um valor de "Custom".</span><span class="sxs-lookup"><span data-stu-id="7ff5b-134">To switch the Windows Media Player control to skin mode, call the **IWMPPlayer::put\_uiMode** method, passing in a value of "custom".</span></span> <span data-ttu-id="7ff5b-135">Especifique o caminho e o nome de arquivo do arquivo de definição de capa a ser usado, retornando-o do método **IWMPRemoteMediaServices:: GetCustomUIMode** .</span><span class="sxs-lookup"><span data-stu-id="7ff5b-135">Specify the path and file name of the skin definition file to use by returning it from the **IWMPRemoteMediaServices::GetCustomUIMode** method.</span></span>

<span data-ttu-id="7ff5b-136">Se você quiser fornecer um objeto programável para comunicação entre sua capa e seu programa, passe um nome e um ponteiro para um ponteiro **IDispatch** como os dois parâmetros de saída do método **IWMPRemoteMediaServices:: GetScriptableObject** .</span><span class="sxs-lookup"><span data-stu-id="7ff5b-136">If you want to provide a scriptable object for communication between your skin and your program, pass a name and a pointer to an **IDispatch** pointer as the two out parameters of the **IWMPRemoteMediaServices::GetScriptableObject** method.</span></span> <span data-ttu-id="7ff5b-137">Em seguida, sua capa pode fazer chamadas para o objeto programável usando o nome especificado como se fosse um atributo global semelhante ao atributo global do **Player** .</span><span class="sxs-lookup"><span data-stu-id="7ff5b-137">Your skin can then make calls to the scriptable object by using the name specified as though it were a global attribute similar to the **player** global attribute.</span></span>

<span data-ttu-id="7ff5b-138">Uma capa aplicada a um controle remoto do Windows Media Player pode acessar o objeto **PlayerApplication** usando outro atributo global chamado **PlayerApplication**.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-138">A skin applied to a remoted Windows Media Player control can access the **PlayerApplication** object using another global attribute called **playerApplication**.</span></span> <span data-ttu-id="7ff5b-139">Como a propriedade **Player. playerApplication** não pode ser acessada por capas, você deve usar esse atributo global quando desejar que o código de sua capa gerencie o encaixe e desencaixe.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-139">Because the **Player.playerApplication** property cannot be accessed by skins, you must use this global attribute when you want your skin code to manage docking and undocking.</span></span>

## <a name="samples"></a><span data-ttu-id="7ff5b-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ff5b-140">Samples</span></span>

<span data-ttu-id="7ff5b-141">O pacote de instalação do SDK do Windows Media Player instala um exemplo que demonstra a aplicação de uma capa ao controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-141">The Windows Media Player SDK setup package installs a sample that demonstrates applying a skin to the Windows Media Player control.</span></span> <span data-ttu-id="7ff5b-142">Consulte o exemplo de RemoteSkin para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7ff5b-142">See the RemoteSkin sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ff5b-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ff5b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ff5b-144">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="7ff5b-144">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="7ff5b-145">**Usando o controle do Windows Media Player em um programa C++**</span><span class="sxs-lookup"><span data-stu-id="7ff5b-145">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




