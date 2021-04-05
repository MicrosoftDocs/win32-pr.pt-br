---
title: Botões (SDK do Windows Media Player)
description: Botões
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Aparências móveis do Windows Media Player, visão geral do botão
- capas, visão geral do botão
- referência para capas, botões
- botões em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085102"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="5533a-107">Botões (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="5533a-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="5533a-108">Você desejará usar um ou mais botões em sua capa, e cada botão deve ser definido no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="5533a-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="5533a-109">Se você não definir um botão nesta seção, sua capa não será capaz de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="5533a-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="5533a-110">A seção de botões do arquivo de definição de capa começa com esta linha:</span><span class="sxs-lookup"><span data-stu-id="5533a-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="5533a-111">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada um dos botões em sua capa.</span><span class="sxs-lookup"><span data-stu-id="5533a-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="5533a-112">Uma linha típica pode ser:</span><span class="sxs-lookup"><span data-stu-id="5533a-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="5533a-113">Observe que esse código deve ser digitado como uma linha que começa com "PlayPause" e termina com "Push @ 160, 98".</span><span class="sxs-lookup"><span data-stu-id="5533a-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="5533a-114">Você pode usar o modelo a seguir para a seção de botões do arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="5533a-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="5533a-115">Novamente, observe que elas devem ser digitadas como linhas únicas, a primeira começando com "// <Function> " e terminando com " &lt; push 2 Image src &gt; ".</span><span class="sxs-lookup"><span data-stu-id="5533a-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="5533a-116">A segunda linha começa com "//----------" e termina com "------------------."</span><span class="sxs-lookup"><span data-stu-id="5533a-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="5533a-117">As informações do botão para cada linha na seção de botão devem aparecer na seguinte ordem.</span><span class="sxs-lookup"><span data-stu-id="5533a-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="5533a-118">Somente as seis primeiras partes da linha são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="5533a-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="5533a-119">As imagens secundárias não são incluídas, a menos que sejam necessárias.</span><span class="sxs-lookup"><span data-stu-id="5533a-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="5533a-120">Função de botão</span><span class="sxs-lookup"><span data-stu-id="5533a-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="5533a-121">Tipo de botão</span><span class="sxs-lookup"><span data-stu-id="5533a-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="5533a-122">Local do botão</span><span class="sxs-lookup"><span data-stu-id="5533a-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="5533a-123">Origem da imagem enviada por push</span><span class="sxs-lookup"><span data-stu-id="5533a-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="5533a-124">Origem da imagem para o botão desabilitado</span><span class="sxs-lookup"><span data-stu-id="5533a-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="5533a-125">Pressione a cor RGB</span><span class="sxs-lookup"><span data-stu-id="5533a-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="5533a-126">Fonte de imagem secundária normal</span><span class="sxs-lookup"><span data-stu-id="5533a-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="5533a-127">Fonte de imagem terciário normal</span><span class="sxs-lookup"><span data-stu-id="5533a-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="5533a-128">Fonte de imagem secundária enviada por push</span><span class="sxs-lookup"><span data-stu-id="5533a-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="5533a-129">Fonte de imagem terciário enviada por push</span><span class="sxs-lookup"><span data-stu-id="5533a-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="5533a-130">Para obter um exemplo de código de botão, consulte a [seção de botão de exemplo](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="5533a-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5533a-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5533a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5533a-132">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="5533a-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




