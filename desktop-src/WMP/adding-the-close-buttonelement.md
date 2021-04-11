---
title: Adicionando o botão fechar
description: Adicionando o botão fechar
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Criando capas, elemento BUTTONelement
- Aparência do Windows Media Player, elemento BUTTONelement
- elemento skins, BUTTONelement
- arquivos de definição de capa, elemento BUTTONelement
- Elemento BUTTONelement
- elementos, BUTTONelement
- Criando capas, botões fechar
- Capas do Windows Media Player, botões fechar
- capas, botões fechar
- arquivos de definição de capa, botões de fechamento
- Botões de fechamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159908"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="96119-114">Adicionando o botão fechar</span><span class="sxs-lookup"><span data-stu-id="96119-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="96119-115">O botão fechar é semelhante em conceito ao botão reproduzir, mas tem códigos e cores diferentes.</span><span class="sxs-lookup"><span data-stu-id="96119-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="96119-116">Coloque o código do **botão** fecharelement após o colchete angular de fechamento do **botão** de reprodução.</span><span class="sxs-lookup"><span data-stu-id="96119-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="96119-117">Os atributos a seguir são usados para definir o **buttonelement** para o botão fechar:</span><span class="sxs-lookup"><span data-stu-id="96119-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="96119-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="96119-118">**mappingColor**</span></span>

<span data-ttu-id="96119-119">Esse é o valor de cor da região no arquivo de arte de mapeamento que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96119-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="96119-120">Nesse caso, é a cor vermelha sólida.</span><span class="sxs-lookup"><span data-stu-id="96119-120">In this case it is the solid red color.</span></span> <span data-ttu-id="96119-121">Esse atributo é necessário para qualquer **buttonelement**.</span><span class="sxs-lookup"><span data-stu-id="96119-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="96119-122">Ao definir essa cor, você está dizendo ao Windows Media Player para associar essa área de cores ao código XML desse botão.</span><span class="sxs-lookup"><span data-stu-id="96119-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="96119-123">**upToolTip**</span><span class="sxs-lookup"><span data-stu-id="96119-123">**upToolTip**</span></span>

<span data-ttu-id="96119-124">Isso define o texto que será exibido quando o usuário passar o mouse sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="96119-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="96119-125">Isso é o mesmo que o botão Executar, exceto que ele é rotulado como "fechar".</span><span class="sxs-lookup"><span data-stu-id="96119-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="96119-126">**onClick**</span><span class="sxs-lookup"><span data-stu-id="96119-126">**onClick**</span></span>

<span data-ttu-id="96119-127">Isso define o evento que ocorre quando o mouse clica no botão.</span><span class="sxs-lookup"><span data-stu-id="96119-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="96119-128">O valor desse atributo de evento é chamado de manipulador de eventos e será uma linha de código do Microsoft JScript ou uma função JScript em um arquivo de texto externo que é carregado pelo atributo **loadscript** de uma **exibição**.</span><span class="sxs-lookup"><span data-stu-id="96119-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="96119-129">Nesse caso, o código JScript chama o método **Close** do elemento **View** usando a **exibição** de atributo global, que fecha a exibição e desliga o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="96119-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96119-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96119-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96119-131">**Criando o arquivo de definição de capa**</span><span class="sxs-lookup"><span data-stu-id="96119-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




