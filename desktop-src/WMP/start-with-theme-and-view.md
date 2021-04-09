---
title: Iniciar com tema e exibição
description: Iniciar com tema e exibição
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Criando capas, elemento THEME
- Capas do Windows Media Player, elemento THEME
- capas, elemento THEME
- arquivos de definição de capa, elemento THEME
- Elemento THEME
- Criando capas, elemento VIEW
- Capas do Windows Media Player, elemento VIEW
- aparência, elemento VIEW
- arquivos de definição de capa, elemento VIEW
- Elemento VIEW
- elementos, exibição
- elementos, tema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822973"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="4baa0-115">Iniciar com tema e exibição</span><span class="sxs-lookup"><span data-stu-id="4baa0-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="4baa0-116">Cada capa deve ter exatamente um elemento **Theme** e pelo menos um elemento **View** .</span><span class="sxs-lookup"><span data-stu-id="4baa0-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="4baa0-117">Usando seu editor de texto, crie o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="4baa0-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="4baa0-118">Deixe algumas linhas em branco antes da marca de **exibição** de fechamento, pois você adicionará mais código aqui mais tarde.</span><span class="sxs-lookup"><span data-stu-id="4baa0-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="4baa0-119">Salve o arquivo com qualquer nome de arquivo que desejar, mas certifique-se de que a extensão seja. WMS.</span><span class="sxs-lookup"><span data-stu-id="4baa0-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="4baa0-120">Por exemplo, um nome de arquivo típico pode ser skinone. WMS.</span><span class="sxs-lookup"><span data-stu-id="4baa0-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="4baa0-121">Cada capa deve começar com <THEME> e terminar com </THEME>.</span><span class="sxs-lookup"><span data-stu-id="4baa0-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="4baa0-122">Você só pode ter um elemento **Theme** em sua capa, mas deve ter um.</span><span class="sxs-lookup"><span data-stu-id="4baa0-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="4baa0-123">Você também deve ter pelo menos um elemento de **exibição** .</span><span class="sxs-lookup"><span data-stu-id="4baa0-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="4baa0-124">Você pode ter mais de uma **exibição**, mas este exemplo tem apenas uma.</span><span class="sxs-lookup"><span data-stu-id="4baa0-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="4baa0-125">Você deve ter uma abertura <VIEW> e um fechamento <VIEW>. Observe que a marca de abertura </VIEW> não fecha a marca imediatamente, mas inclui vários atributos antes do colchete angular de fechamento (>).</span><span class="sxs-lookup"><span data-stu-id="4baa0-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="4baa0-126">Os seguintes atributos são usados no elemento **Theme** neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="4baa0-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="4baa0-127">**clippingColor**</span><span class="sxs-lookup"><span data-stu-id="4baa0-127">**clippingColor**</span></span>

<span data-ttu-id="4baa0-128">Nem sempre será necessário o atributo **clippingColor** se as bordas da sua capa forem retangulares.</span><span class="sxs-lookup"><span data-stu-id="4baa0-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="4baa0-129">A capa neste exemplo é formada por oval, portanto, você precisa de uma cor de recorte para as partes da capa para as quais você deseja ver a área de trabalho; essencialmente, todas as partes fora da oval.</span><span class="sxs-lookup"><span data-stu-id="4baa0-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="4baa0-130">Nesta capa de exemplo, usaremos um amarelo escuro, especificado como " \# CCCC00" no formato da Web.</span><span class="sxs-lookup"><span data-stu-id="4baa0-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="4baa0-131">Os motivos para essa escolha são fornecidos na [criação do arquivo de arte principal](creating-the-primary-art-file.md).</span><span class="sxs-lookup"><span data-stu-id="4baa0-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="4baa0-132">Essencialmente, esse valor sempre será um número que você obtém do seu programa de arte.</span><span class="sxs-lookup"><span data-stu-id="4baa0-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="4baa0-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="4baa0-133">**backgroundImage**</span></span>

<span data-ttu-id="4baa0-134">Esse é o nome do arquivo de arte primário.</span><span class="sxs-lookup"><span data-stu-id="4baa0-134">This is the name of the primary art file.</span></span> <span data-ttu-id="4baa0-135">Deve ser o nome exato do arquivo e o caminho do seu arquivo de arte primário.</span><span class="sxs-lookup"><span data-stu-id="4baa0-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="4baa0-136">Somente arquivos BMP, JPG, GIF e PNG têm suporte e o BMP é recomendado.</span><span class="sxs-lookup"><span data-stu-id="4baa0-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="4baa0-137">**titleBar**</span><span class="sxs-lookup"><span data-stu-id="4baa0-137">**titleBar**</span></span>

<span data-ttu-id="4baa0-138">Essa capa não tem uma **TitleBar**, portanto, o valor será "false".</span><span class="sxs-lookup"><span data-stu-id="4baa0-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="4baa0-139">Você só desejará uma barra de título se quiser que sua capa tenha uma cor de plano de fundo e seja retangular.</span><span class="sxs-lookup"><span data-stu-id="4baa0-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="4baa0-140">Certifique-se de colocar o colchete angular de fechamento (>) após o valor da **TitleBar** para indicar que você terminou de definir a **exibição**.</span><span class="sxs-lookup"><span data-stu-id="4baa0-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="4baa0-141">Deixe algumas linhas em branco antes da **exibição** de fechamento e das marcas de **tema** .</span><span class="sxs-lookup"><span data-stu-id="4baa0-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="4baa0-142">Você precisará das linhas para o código que será adicionado posteriormente.</span><span class="sxs-lookup"><span data-stu-id="4baa0-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4baa0-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4baa0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4baa0-144">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="4baa0-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




