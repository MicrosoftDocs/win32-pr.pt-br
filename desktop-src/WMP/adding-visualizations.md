---
title: Adicionando visualizações
description: Adicionando visualizações
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Criando capas, visualizações
- Capas do Windows Media Player, visualizações
- capas, visualizações
- visualizações, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635997"
---
# <a name="adding-visualizations"></a><span data-ttu-id="c2742-107">Adicionando visualizações</span><span class="sxs-lookup"><span data-stu-id="c2742-107">Adding Visualizations</span></span>

<span data-ttu-id="c2742-108">Você pode adicionar uma janela de visualização da mesma maneira que adicionou uma janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2742-108">You can add a visualization window the same way you added a video window.</span></span> <span data-ttu-id="c2742-109">A mesma capa pode ser usada, mas um elemento **Effects** é usado.</span><span class="sxs-lookup"><span data-stu-id="c2742-109">The same skin can be used, but an **EFFECTS** element is used.</span></span>

<span data-ttu-id="c2742-110">Primeiro, você deve adicionar o elemento **Effects** e dar a ele uma ID e um tamanho:</span><span class="sxs-lookup"><span data-stu-id="c2742-110">First you must add the **EFFECTS** element and give it an ID and size:</span></span>


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



<span data-ttu-id="c2742-111">Em seguida, você pode atribuir os dois botões uma cadeia de caracteres de código de visualização anterior e seguinte:</span><span class="sxs-lookup"><span data-stu-id="c2742-111">Then you can assign the two buttons a previous and next visualization code string:</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



<span data-ttu-id="c2742-112">As camadas e os bitmaps eram os mesmos usados no exemplo de vídeo, exceto que a seta de reprodução foi copiada e invertida horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c2742-112">The layers and bitmaps were the same ones used in the video example, except that the play arrow was copied and flipped horizontally.</span></span>

<span data-ttu-id="c2742-113">Por fim, um elemento **Player** simples com o atributo **URL** foi adicionado para escolher uma música a ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="c2742-113">Finally, a simple **PLAYER** element with the **URL** attribute was added to choose a song to play.</span></span>


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



<span data-ttu-id="c2742-114">Você pode ver uma aparência de visualização de trabalho semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="c2742-114">You can see a similar working visualization skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2742-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2742-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2742-116">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="c2742-116">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




