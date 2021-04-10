---
title: Usando o controle do Windows Media Player em um programa C++
description: Usando o controle do Windows Media Player em um programa C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160112"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="bfe7e-119">Usando o controle do Windows Media Player em um programa C++</span><span class="sxs-lookup"><span data-stu-id="bfe7e-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="bfe7e-120">O uso do C++ para inserir o controle do Windows Media Player tem suporte no Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="bfe7e-121">Há várias maneiras diferentes de usar o controle do Windows Media Player em um programa C++.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="bfe7e-122">Você pode criar uma instância do controle em um aplicativo de console ou pode inserir o controle em um aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="bfe7e-123">Além disso, você pode implementar interfaces que permitem executar um controle de player incorporado no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="bfe7e-124">Você pode personalizar a interface do usuário de um controle inserido aplicando um arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="bfe7e-125">Essas informações são descritas nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="bfe7e-126">Tópico</span><span class="sxs-lookup"><span data-stu-id="bfe7e-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="bfe7e-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="bfe7e-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfe7e-128">Usando o controle do Windows Media Player em um aplicativo de console</span><span class="sxs-lookup"><span data-stu-id="bfe7e-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="bfe7e-129">Descreve um aplicativo de console C++ simples que instancia o controle do Windows Media Player para exibir a versão.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="bfe7e-130">Hospedando o controle do Windows Media Player em um aplicativo do Windows</span><span class="sxs-lookup"><span data-stu-id="bfe7e-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="bfe7e-131">Descreve como usar a janela do host ActiveX do ATL para inserir o controle do Windows Media Player em um programa do Windows.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="bfe7e-132">Estabelecer comunicação remota do controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bfe7e-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="bfe7e-133">Descreve como inserir o controle do Windows Media Player em um programa C++ no modo remoto, o que permite que os usuários desencaixem o controle para alternar para o modo completo do Player.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="bfe7e-134">Manipulando eventos em C++</span><span class="sxs-lookup"><span data-stu-id="bfe7e-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="bfe7e-135">Descreve como receber notificações de eventos do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="bfe7e-136">Usando capas com o controle do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="bfe7e-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="bfe7e-137">Descreve como aplicar um arquivo de capa a um controle do Windows Media Player incorporado em um programa C++.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="bfe7e-138">Você pode inserir o controle móvel do Windows Media Player 10 em um aplicativo Windows CE.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="bfe7e-139">As técnicas que você usa para fazer isso são semelhantes às usadas com o controle Windows Media Player da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="bfe7e-140">No entanto, há diferenças entre ATL para Windows e ATL para Windows CE.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="bfe7e-141">Esta documentação descreve as diferenças entre essas implementações, quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="bfe7e-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bfe7e-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfe7e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfe7e-143">**Referência de modelo de objeto para C++**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="bfe7e-144">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="bfe7e-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




