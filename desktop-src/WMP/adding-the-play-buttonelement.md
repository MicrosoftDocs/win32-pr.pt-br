---
title: Adicionando o botão de reprodução
description: Adicionando o botão de reprodução
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Criando capas, elemento BUTTONelement
- Aparência do Windows Media Player, elemento BUTTONelement
- elemento skins, BUTTONelement
- arquivos de definição de capa, elemento BUTTONelement
- Elemento BUTTONelement
- elementos, BUTTONelement
- Criando capas, botões de reprodução
- Capas do Windows Media Player, botões de reprodução
- capas, botões de reprodução
- arquivos de definição de capa, botões de reprodução
- Botões de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498710"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="617ec-114">Adicionando o botão de reprodução</span><span class="sxs-lookup"><span data-stu-id="617ec-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="617ec-115">Por fim, você pode adicionar os elementos **buttonelement** que conectam os botões visuais na tela às ações do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="617ec-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="617ec-116">Esse é o núcleo da sua capa e você pode considerá-la como cabeamento da superfície da capa para a maquina interna do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="617ec-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="617ec-117">O **buttonelement** s está contido em um **Button**.</span><span class="sxs-lookup"><span data-stu-id="617ec-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="617ec-118">Você deve sempre ter pelo menos um **buttonelement** dentro de cada um dos **botões**.</span><span class="sxs-lookup"><span data-stu-id="617ec-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="617ec-119">Coloque o código do **botão** de execução após o colchete angular de fechamento do **botão**.</span><span class="sxs-lookup"><span data-stu-id="617ec-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="617ec-120">Os atributos a seguir são usados para definir o **buttonelement** para o botão Play:</span><span class="sxs-lookup"><span data-stu-id="617ec-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="617ec-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="617ec-121">**mappingColor**</span></span>

<span data-ttu-id="617ec-122">Esse é o valor de cor de uma região no arquivo de arte de mapeamento que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="617ec-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="617ec-123">Nesse caso, é a cor verde sólida.</span><span class="sxs-lookup"><span data-stu-id="617ec-123">In this case it is the solid green color.</span></span> <span data-ttu-id="617ec-124">Esse atributo é necessário para qualquer **buttonelement**.</span><span class="sxs-lookup"><span data-stu-id="617ec-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="617ec-125">Ao definir essa cor, você está dizendo ao Windows Media Player para associar essa área de cores ao código XML desse botão.</span><span class="sxs-lookup"><span data-stu-id="617ec-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="617ec-126">**upToolTip**</span><span class="sxs-lookup"><span data-stu-id="617ec-126">**upToolTip**</span></span>

<span data-ttu-id="617ec-127">Isso define o texto que será exibido se o usuário passar o mouse sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="617ec-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="617ec-128">Não confunda isso com a arte de foco que será exibida.</span><span class="sxs-lookup"><span data-stu-id="617ec-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="617ec-129">Uma dica de ferramenta é uma pequena legenda de balão que leva um tempo para aparecer.</span><span class="sxs-lookup"><span data-stu-id="617ec-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="617ec-130">No entanto, a imagem de arte em foco será exibida instantaneamente em qualquer cor e forma que você escolher.</span><span class="sxs-lookup"><span data-stu-id="617ec-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="617ec-131">**onClick**</span><span class="sxs-lookup"><span data-stu-id="617ec-131">**onClick**</span></span>

<span data-ttu-id="617ec-132">Isso define o evento que ocorre quando o mouse clica no botão.</span><span class="sxs-lookup"><span data-stu-id="617ec-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="617ec-133">O valor desse atributo de evento é chamado de manipulador de eventos e será uma linha de código do Microsoft JScript ou uma função JScript em um arquivo de texto externo que é carregado pelo atributo **loadscript** de uma **exibição**.</span><span class="sxs-lookup"><span data-stu-id="617ec-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="617ec-134">Nesse caso, o código JScript chama o método de **URL** do Windows Media Player, que carrega e começa a reproduzir um arquivo chamado "Laure. WMA".</span><span class="sxs-lookup"><span data-stu-id="617ec-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="617ec-135">Observe que a linha termina com um ponto e vírgula dentro das aspas, o que é uma boa prática de codificação JScript.</span><span class="sxs-lookup"><span data-stu-id="617ec-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="617ec-136">Observe também o uso de aspas simples dentro das aspas duplas para definir o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="617ec-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="617ec-137">Para obter mais informações sobre o JScript, consulte [usando o JScript](using-jscript.md) na seção sobre capas deste SDK.</span><span class="sxs-lookup"><span data-stu-id="617ec-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="617ec-138">Observe que não há nenhuma marca **buttonelement** final.</span><span class="sxs-lookup"><span data-stu-id="617ec-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="617ec-139">Se um elemento não incluir outro elemento, você poderá fechá-lo com a barra invertida logo antes do colchete angular de fechamento.</span><span class="sxs-lookup"><span data-stu-id="617ec-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="617ec-140">Isso informa ao XML que você terminou com esse elemento.</span><span class="sxs-lookup"><span data-stu-id="617ec-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="617ec-141">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="617ec-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="617ec-142">e</span><span class="sxs-lookup"><span data-stu-id="617ec-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="617ec-143">Transmita as mesmas informações em XML.</span><span class="sxs-lookup"><span data-stu-id="617ec-143">convey the same information in XML.</span></span>

<span data-ttu-id="617ec-144">O poder das capas vem do uso de manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="617ec-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="617ec-145">Se o usuário fizer algo com um mouse, você poderá manipular esse evento com o JScript.</span><span class="sxs-lookup"><span data-stu-id="617ec-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="617ec-146">Seu código pode ser uma única linha que faz com que o Windows Media Player faça algo simples como reproduzir, ou pode ser um aplicativo completo escrito em JScript.</span><span class="sxs-lookup"><span data-stu-id="617ec-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="617ec-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="617ec-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="617ec-148">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="617ec-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




