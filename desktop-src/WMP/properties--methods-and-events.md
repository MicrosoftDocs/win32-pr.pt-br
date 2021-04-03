---
title: Propriedades, métodos e eventos
description: Propriedades, métodos e eventos
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, propriedades do modelo de objeto
- Windows Media Player, métodos para modelo de objeto
- Windows Media Player, eventos para modelo de objeto
- Modelo de objeto do Windows Media Player, propriedades
- Modelo de objeto do Windows Media Player, métodos
- Modelo de objeto do Windows Media Player, eventos
- modelo de objeto, propriedades
- modelo de objeto, métodos
- modelo de objeto, eventos
- Controle ActiveX do Windows Media Player, propriedades do modelo de objeto
- Controle ActiveX, propriedades do modelo de objeto
- Controle ActiveX móvel do Windows Media Player, propriedades do modelo de objeto
- Windows Media Player Mobile, propriedades para modelo de objeto
- Controle ActiveX do Windows Media Player, métodos para modelo de objeto
- Controle ActiveX, métodos para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, métodos para modelo de objeto
- Windows Media Player Mobile, métodos para modelo de objeto
- Controle ActiveX do Windows Media Player, eventos para modelo de objeto
- Controle ActiveX, eventos para o modelo de objeto
- Controle ActiveX móvel do Windows Media Player, eventos para modelo de objeto
- Windows Media Player Mobile, eventos para modelo de objeto
- Propriedades, modelo de objeto do Windows Media Player
- métodos, modelo de objeto do Windows Media Player
- eventos, modelo de objeto do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084087"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="d02c9-127">Propriedades, métodos e eventos</span><span class="sxs-lookup"><span data-stu-id="d02c9-127">Properties, Methods and Events</span></span>

<span data-ttu-id="d02c9-128">Cada objeto tem métodos e propriedades por meio dos quais você pode programar o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d02c9-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="d02c9-129">Um método é uma ação que o objeto pode tomar.</span><span class="sxs-lookup"><span data-stu-id="d02c9-129">A method is an action that the object can take.</span></span> <span data-ttu-id="d02c9-130">Uma propriedade é um valor de dados que você pode ler ou alterar.</span><span class="sxs-lookup"><span data-stu-id="d02c9-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="d02c9-131">Por exemplo, o método **Play** inicia o conteúdo que está sendo reproduzido e **a propriedade** ratename indica a taxa de quadros atual do conteúdo que está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="d02c9-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="d02c9-132">Além disso, o objeto **Player** gera eventos que oferecem a oportunidade de executar ações em momentos específicos.</span><span class="sxs-lookup"><span data-stu-id="d02c9-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="d02c9-133">Você escreve o código em um manipulador de eventos que será executado quando o Windows Media Player gerar o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d02c9-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="d02c9-134">Por exemplo, você pode escrever código em um manipulador de eventos **PlayStateChange** que determina se a alteração no estado é que a mídia foi encerrada e, em caso afirmativo, exibe uma caixa de diálogo perguntando os usuários se eles desejam reproduzir a mídia novamente.</span><span class="sxs-lookup"><span data-stu-id="d02c9-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="d02c9-135">Todos os métodos no modelo de objeto do Windows Media Player são assíncronos.</span><span class="sxs-lookup"><span data-stu-id="d02c9-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="d02c9-136">Se você chamar dois métodos no mesmo procedimento, o segundo método não poderá confiar no primeiro método que concluiu sua ação.</span><span class="sxs-lookup"><span data-stu-id="d02c9-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d02c9-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d02c9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02c9-138">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="d02c9-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




