---
title: Seção de botões
description: Seção de botões
ms.assetid: fa413bb4-e04a-4e3d-9754-cd4c2d82de6e
keywords:
- Capas do Windows Media Player Mobile, seção de botões
- capas, seção de botões
- Criando capas, seção de botões
- escrevendo código para capas, seção de botões
- botões em capas, seção de botões
- arquivos de definição de capa, seção de botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f994225154e3f4cc55070351c32c654d5ad616c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005738"
---
# <a name="buttons-section"></a><span data-ttu-id="d5b98-109">Seção de botões</span><span class="sxs-lookup"><span data-stu-id="d5b98-109">Buttons Section</span></span>

<span data-ttu-id="d5b98-110">Em seguida, você deve definir os botões que você usará:</span><span class="sxs-lookup"><span data-stu-id="d5b98-110">Next, you must define the buttons you will be using:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   100,20,110,100 Pushed @ 100,20   Disabled @ 100,20    0,255,255  Pushed @ 270,20     Pushed @ 270,130
    Stop       PushHit    20,20,45,45    Pushed @ 20,20    Disabled @ 20,20   255,255,  0
    Next       PushHit    20,80,45,45    Pushed @ 20,80    Disabled @ 20,80   255,  0,  0
    Prev       PushHit    20,140,45,45   Pushed @ 20,140   Disabled @ 20,130    0,  0,255

```



<span data-ttu-id="d5b98-111">Há quatro botões definidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="d5b98-111">There are four buttons defined in this section.</span></span> <span data-ttu-id="d5b98-112">A página que você está exibindo pode encapsular essas linhas, mas ao digitar o código, você não deve quebrar linhas automaticamente; ou seja, cada linha deve estar completa e terminar com uma marca de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="d5b98-112">The page you are viewing may wrap these lines, but when you type in the code, you must not wrap lines; that is, each line must be complete and end with a paragraph mark.</span></span>

> [!Note]  
> <span data-ttu-id="d5b98-113">Os tipos de botões são preteridos nas capas do Windows Media Player 10 Mobile ou posteriores.</span><span class="sxs-lookup"><span data-stu-id="d5b98-113">Buttons types are deprecated in Windows Media Player 10 Mobile or later skins.</span></span> <span data-ttu-id="d5b98-114">Em vez de um tipo de botão declarado em seu arquivo de capa, digite "NA" para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="d5b98-114">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

<span data-ttu-id="d5b98-115">Para cada botão, você deve definir a função, o tipo, o local, a fonte da imagem enviada, a fonte desabilitada e a cor (para botões de tipo de clique).</span><span class="sxs-lookup"><span data-stu-id="d5b98-115">For each button you must define the function, type, location, pushed image source, disabled source, and color (for hit-type buttons).</span></span> <span data-ttu-id="d5b98-116">Além disso, para o botão PlayPause, você deve definir as fontes de imagem normais e enviadas por push para o estado pausado.</span><span class="sxs-lookup"><span data-stu-id="d5b98-116">In addition, for the PlayPause button, you must define the normal and pushed image sources for the paused state.</span></span>

<span data-ttu-id="d5b98-117">Para obter mais informações sobre a seção de botões do arquivo de definição de capa, consulte [botões](buttons.md) na referência de capa.</span><span class="sxs-lookup"><span data-stu-id="d5b98-117">For more about the Buttons section of the skin definition file, see [Buttons](buttons.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5b98-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b98-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b98-119">**Escrevendo o código**</span><span class="sxs-lookup"><span data-stu-id="d5b98-119">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




