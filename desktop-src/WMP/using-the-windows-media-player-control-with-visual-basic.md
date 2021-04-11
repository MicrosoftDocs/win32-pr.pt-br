---
title: Usando o controle do Windows Media Player com Visual Basic
description: Usando o controle do Windows Media Player com Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, Visual Basic
- Modelo de objeto do Windows Media Player, Visual Basic
- modelo de objeto, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Controle ActiveX do Windows Media Player, Visual Basic
- Controle ActiveX móvel do Windows Media Player, Visual Basic
- Controle ActiveX, Visual Basic
- Incorporação de programas baseados em Visual Basic
- incorporação, programas baseados em Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292398"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a><span data-ttu-id="bdbd8-119">Usando o controle do Windows Media Player com Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bdbd8-119">Using the Windows Media Player Control with Visual Basic</span></span>

<span data-ttu-id="bdbd8-120">Esta seção descreve como usar o controle ActiveX do Windows Media Player 9 Series ou posterior em aplicativos criados com o Microsoft Visual Basic 6,0.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-120">This section describes how to use the Windows Media Player 9 Series or later ActiveX control in applications created with Microsoft Visual Basic 6.0.</span></span>

## <a name="getting-started"></a><span data-ttu-id="bdbd8-121">Introdução</span><span class="sxs-lookup"><span data-stu-id="bdbd8-121">Getting Started</span></span>

<span data-ttu-id="bdbd8-122">Para adicionar o controle do Windows Media Player à caixa de ferramentas, primeiro selecione **componentes** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-122">To add the Windows Media Player control to the toolbox, first select **Components** from the **Project** menu.</span></span> <span data-ttu-id="bdbd8-123">Na caixa de diálogo componentes, marque a caixa de seleção ao lado de "Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="bdbd8-123">In the Components dialog box, select the check box next to "Windows Media Player".</span></span> <span data-ttu-id="bdbd8-124">Na parte inferior da caixa de diálogo, confirme se o arquivo selecionado está wmp.dll.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-124">At the bottom of the dialog box, confirm that the selected file is wmp.dll.</span></span> <span data-ttu-id="bdbd8-125">Depois de fechar a caixa de diálogo, você pode colocar uma instância do controle do Windows Media Player no formulário de maneira usual.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-125">After closing the dialog box, you can place an instance of the Windows Media Player control on your form in the usual ways.</span></span>

<span data-ttu-id="bdbd8-126">Você pode definir muitas propriedades de controle usando o janela Propriedades.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-126">You can set many control properties using the Properties window.</span></span> <span data-ttu-id="bdbd8-127">Para definir algumas propriedades, você deve usar a caixa de diálogo Propriedades do Windows Media Player, que você abre usando o item "(personalizado)" no janela Propriedades.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-127">To set some properties you must use the Windows Media Player Properties dialog box, which you open using the "(Custom)" item in the Properties window.</span></span>

## <a name="object-references"></a><span data-ttu-id="bdbd8-128">Referências de objeto</span><span class="sxs-lookup"><span data-stu-id="bdbd8-128">Object References</span></span>

<span data-ttu-id="bdbd8-129">Você usa determinadas propriedades de controle do Player para obter referências a objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-129">You use certain Player control properties to get references to particular objects.</span></span> <span data-ttu-id="bdbd8-130">Por exemplo, a propriedade **cdromCollection** retorna uma referência a um objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-130">For example, the **cdromCollection** property returns a reference to a **CdromCollection** object.</span></span> <span data-ttu-id="bdbd8-131">Você deve atribuir tal referência a uma variável que você declarou como a interface correspondente.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-131">You must assign such a reference to a variable that you declared as the corresponding interface.</span></span> <span data-ttu-id="bdbd8-132">No caso da propriedade **cdromCollection** , por exemplo, você atribui seu valor de retorno a uma variável do tipo **IWMPCdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-132">In the case of the **cdromCollection** property, for example, you assign its return value to a variable of type **IWMPCdromCollection**.</span></span>

<span data-ttu-id="bdbd8-133">Leia o tópico [interfaces](interfaces.md) na [referência do modelo de objeto para C++](object-model-reference-for-c.md) para identificar quais objetos implementam várias interfaces.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-133">Read the [Interfaces](interfaces.md) topic in the [Object Model Reference for C++](object-model-reference-for-c.md) to identify which objects implement multiple interfaces.</span></span> <span data-ttu-id="bdbd8-134">Nesses casos, você deve declarar uma variável de objeto como a interface de numeração mais alta documentada neste SDK para ter acesso a todas as propriedades e métodos desse objeto.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-134">In those cases, you must declare an object variable as the highest-numbered interface documented in this SDK to have access to all of the properties and methods of that object.</span></span> <span data-ttu-id="bdbd8-135">Por exemplo, você deve atribuir o valor da propriedade **currentMedia** de controle do Windows Media Player a uma variável declarada como **IWMPMedia3** para garantir que você tenha acesso aos métodos **getAttributeCountByType** e **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-135">For example, you should assign the value of the Windows Media Player control **currentMedia** property to a variable declared as **IWMPMedia3** to assure that you have access to the **getAttributeCountByType** and **getItemInfoByType** methods.</span></span>

> [!Note]  
> <span data-ttu-id="bdbd8-136">O objeto **WindowsMediaPlayer** implementa todas as propriedades e métodos das interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** e **IWMPPlayer4** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-136">The **WindowsMediaPlayer** object implements all of the properties and methods of the **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3**, and **IWMPPlayer4** interfaces.</span></span> <span data-ttu-id="bdbd8-137">Você não precisa declarar variáveis separadas para qualquer uma dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-137">You do not need to declare separate variables for any of these interfaces.</span></span> <span data-ttu-id="bdbd8-138">Você pode acessar todos os seus membros usando o nome que você atribuiu à sua instância do **WindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-138">You can access all of their members using the name you assigned to your **WindowsMediaPlayer** instance.</span></span>

 

<span data-ttu-id="bdbd8-139">No Pesquisador de objetos do Visual Basic, você verá muitas interfaces destinadas ao uso privado pelo controle do Windows Media Player, incluindo algumas que dão suporte a desenvolvedores de capas.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-139">In the Visual Basic Object Browser you will see many interfaces that are intended for private use by the Windows Media Player control, including some that support skin developers.</span></span> <span data-ttu-id="bdbd8-140">Você deve usar somente os objetos, as propriedades, os métodos e os eventos documentados neste SDK.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-140">You should use only the objects, properties, methods, and events that are documented in this SDK.</span></span>

## <a name="additional-tips"></a><span data-ttu-id="bdbd8-141">Dicas Adicionais</span><span class="sxs-lookup"><span data-stu-id="bdbd8-141">Additional Tips</span></span>

-   <span data-ttu-id="bdbd8-142">A documentação de referência mostra a sintaxe do JScript.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-142">The reference documentation shows JScript syntax.</span></span> <span data-ttu-id="bdbd8-143">No JScript, os argumentos passados para os métodos são sempre colocados entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-143">In JScript, arguments passed to methods are always enclosed in parentheses.</span></span> <span data-ttu-id="bdbd8-144">No Visual Basic 6,0, os argumentos passados para métodos que não retornam um valor não devem ser colocados entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-144">In Visual Basic 6.0, arguments passed to methods that do not return a value must not be enclosed in parentheses.</span></span>
-   <span data-ttu-id="bdbd8-145">Algumas propriedades ou métodos podem não aparecer no recurso de conclusão de código de lista automática no editor de código de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-145">Some properties or methods may not appear in the Auto List code-completion feature in the Visual Basic code editor.</span></span> <span data-ttu-id="bdbd8-146">Você ainda pode usar esses membros digitando seus nomes exatamente como aparecem nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-146">You can still use those members by typing their names exactly as they appear in this documentation.</span></span>
-   <span data-ttu-id="bdbd8-147">Gerencie a aparência visual do controle usando a propriedade **UIMODE** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-147">Manage the visual appearance of the control using the **uimode** property.</span></span> <span data-ttu-id="bdbd8-148">Você pode fazer isso de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-148">You can do so in two ways.</span></span> <span data-ttu-id="bdbd8-149">Você pode usar a lista suspensa **selecionar um modo** na caixa de diálogo Propriedades do Windows Media Player ou pode digitar o valor correto no janela Propriedades.</span><span class="sxs-lookup"><span data-stu-id="bdbd8-149">You can use the **Select a mode** drop-down list in the Windows Media Player Properties dialog box, or you can type the correct value in the Properties window.</span></span>

    <span data-ttu-id="bdbd8-150">Em particular, não use a propriedade **Visible** para ocultar o controle; em vez disso, atribua o valor "invisível" à propriedade **UIMODE** .</span><span class="sxs-lookup"><span data-stu-id="bdbd8-150">In particular, do not use the **visible** property to hide the control; instead, assign the value "invisible" to the **uimode** property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdbd8-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdbd8-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdbd8-152">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="bdbd8-152">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




