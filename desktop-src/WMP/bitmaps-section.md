---
title: Seção bitmaps
description: Seção bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Capas do Windows Media Player Mobile, bitmaps
- capas, bitmaps
- Criando capas, seção bitmaps
- escrevendo código para capas, seção bitmaps
- bitmaps em capas, seção bitmaps
- arquivos de definição de capa, seção bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005435"
---
# <a name="bitmaps-section"></a><span data-ttu-id="34efb-109">Seção bitmaps</span><span class="sxs-lookup"><span data-stu-id="34efb-109">Bitmaps Section</span></span>

<span data-ttu-id="34efb-110">Em seguida, você deve ter uma seção que define cada um dos seus arquivos de bitmap.</span><span class="sxs-lookup"><span data-stu-id="34efb-110">Next, you must have a section that defines each of your bitmap files.</span></span> <span data-ttu-id="34efb-111">Cada tipo de bitmap que você usará deve ter um arquivo atribuído a ele, embora você possa ter mais de um tipo usando o mesmo bitmap.</span><span class="sxs-lookup"><span data-stu-id="34efb-111">Each type of bitmap you will use must have a file assigned to it, though you can have more than one type using the same bitmap.</span></span>


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="34efb-112">A seção bitmaps deve começar com os bitmaps do Word entre colchetes e, em seguida, uma linha para cada tipo de bitmap que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="34efb-112">The Bitmaps section must begin with the word Bitmaps in brackets and then a line for each bitmap type you want to define.</span></span> <span data-ttu-id="34efb-113">Neste exemplo, cinco tipos de bitmaps foram definidos.</span><span class="sxs-lookup"><span data-stu-id="34efb-113">In this example, five types of bitmaps were defined.</span></span> <span data-ttu-id="34efb-114">Para obter mais informações sobre a seção bitmaps, consulte [bitmaps](bitmaps.md) na referência de capa.</span><span class="sxs-lookup"><span data-stu-id="34efb-114">For more about the Bitmaps section, see [Bitmaps](bitmaps.md) in the Skin Reference.</span></span>

> [!Note]  
> <span data-ttu-id="34efb-115">A região e super bitmaps são preteridos nas capas do Windows Media Player 10 Mobile ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="34efb-115">The Region and Super bitmaps are deprecated in Windows Media Player 10 Mobile or later skins.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="34efb-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34efb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34efb-117">**Escrevendo o código**</span><span class="sxs-lookup"><span data-stu-id="34efb-117">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




