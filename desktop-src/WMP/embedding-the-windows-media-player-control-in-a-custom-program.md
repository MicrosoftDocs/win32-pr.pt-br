---
title: Inserindo o controle do Windows Media Player em um programa personalizado
description: Inserindo o controle do Windows Media Player em um programa personalizado
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Windows Media Player Mobile, inserindo controle ActiveX
- incorporação, programas personalizados
- inserção de programa personalizada
- incorporação, programas baseados em Visual Basic
- Incorporação de programas baseados em Visual Basic
- inserindo, manualmente usando métodos COM
- inserção manual usando métodos COM
- incorporando, programas em C++
- Incorporação de programa C++
- incorporando, programas do Visual Studio
- Visual Studio, incorporação de programa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005294"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="0c4b6-120">Inserindo o controle do Windows Media Player em um programa personalizado</span><span class="sxs-lookup"><span data-stu-id="0c4b6-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="0c4b6-121">Como o controle ActiveX do Windows Media Player é baseado na tecnologia Microsoft Component Object Model (COM), você pode incorporá-lo em programas escritos com muitas linguagens de programação diferentes.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="0c4b6-122">O controle do Windows Media Player representa uma maneira fácil de adicionar uma funcionalidade de mídia digital sofisticada a qualquer programa.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="0c4b6-123">No Microsoft Visual Basic, você pode adicionar o controle à caixa de ferramentas de controle, colocá-lo em um formulário e ajustar as propriedades de controle na janela Propriedades.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="0c4b6-124">Se você quiser uma interface de usuário personalizada, poderá posicionar os botões de comando no formulário e adicionar o código que gerencia o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="0c4b6-125">A inserção do controle em um programa baseado em Visual Basic é muito semelhante a incorporá-lo em um documento do Office e sua programação com o VBA.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="0c4b6-126">Como alternativa, você pode inserir o controle manualmente usando métodos COM para instanciar o controle e acessar as interfaces COM documentadas em [referência de modelo de objeto para C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="0c4b6-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="0c4b6-127">Ao inserir o controle do Windows Media Player em um programa C++, você tem a opção de implementar interfaces COM que permitem que o controle seja executado no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="0c4b6-128">Isso significa que o controle incorporado compartilha o mesmo mecanismo de reprodução que o modo completo do Player, e os usuários podem alternar entre o modo completo e o estado encaixado sem interromper a reprodução de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="0c4b6-129">Você também pode controlar o que é exibido nos vários painéis do player de modo completo quando os usuários alternam para o estado desencaixado.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="0c4b6-130">Com a incorporação de C++, você também tem a opção de aplicar um arquivo de definição de capa ao controle do player incorporado.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="0c4b6-131">Essa é uma maneira fácil de criar um código de interface de usuário leve que você pode manter separadamente do código do programa principal.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="0c4b6-132">O Microsoft Visual Studio dá suporte à inserção de controles ActiveX, incluindo o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="0c4b6-133">Quando você opta por fazer isso, o Visual Studio cria um novo assembly de interoperabilidade alternativo (Interop) para gerenciar a interoperabilidade entre o .NET Framework e o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="0c4b6-134">O Visual Studio usa a ferramenta de tlbimp.exe de .NET Framework para criar o assembly de interoperabilidade.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="0c4b6-135">Isso significa que as assinaturas exibidas ao usar o recurso IntelliSense no Visual Studio usam semântica determinada pela versão atual do Tlbimp.</span><span class="sxs-lookup"><span data-stu-id="0c4b6-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c4b6-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c4b6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c4b6-137">**Inserindo o controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="0c4b6-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="0c4b6-138">**Usando o controle do Windows Media Player em um programa C++**</span><span class="sxs-lookup"><span data-stu-id="0c4b6-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="0c4b6-139">**Usando o controle do Windows Media Player em uma solução de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="0c4b6-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="0c4b6-140">**Usando o controle do Windows Media Player com Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="0c4b6-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




