---
title: Descrição (SDK do Windows Media Player)
description: Descrição
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Capas móveis do Windows Media Player, seção Descrição
- capas, seção de descrição
- referência para capas, seção de descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção de descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369126"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="e4b49-108">Descrição (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="e4b49-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="e4b49-109">Ao criar uma capa para o Windows Media Player 9 Series para Windows Mobile 2003 ou posterior, você deve incluir uma seção de descrição.</span><span class="sxs-lookup"><span data-stu-id="e4b49-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="e4b49-110">A seção Descrição permite que você especifique a largura e a altura da exibição, a resolução de vídeo e a orientação de exibição para a qual a capa foi projetada.</span><span class="sxs-lookup"><span data-stu-id="e4b49-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="e4b49-111">A seção descrição deve aparecer no arquivo de definição de capa antes de qualquer outra seção e logo após a declaração de versão inicial.</span><span class="sxs-lookup"><span data-stu-id="e4b49-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="e4b49-112">A seção de descrição do arquivo de definição de capa deve começar com a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="e4b49-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="e4b49-113">Em seguida, você deve adicionar informações sobre as dimensões da capa e a resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="e4b49-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="e4b49-114">O exemplo a seguir mostra como especificar dimensões:</span><span class="sxs-lookup"><span data-stu-id="e4b49-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="e4b49-115">Isso especifica que você criou a capa a ser exibida em 240 pixels de largura, 320 pixels de altura e usando a resolução de vídeo de 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="e4b49-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="e4b49-116">Observe que isso implica em uma orientação de modo retrato.</span><span class="sxs-lookup"><span data-stu-id="e4b49-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="e4b49-117">Opcionalmente, você pode especificar o modo de orientação para o qual você criou a capa na seção Descrição.</span><span class="sxs-lookup"><span data-stu-id="e4b49-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="e4b49-118">O exemplo a seguir mostra como especificar a orientação:</span><span class="sxs-lookup"><span data-stu-id="e4b49-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="e4b49-119">A tabela a seguir lista os valores que você pode usar para orientação.</span><span class="sxs-lookup"><span data-stu-id="e4b49-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="e4b49-120">Orientação</span><span class="sxs-lookup"><span data-stu-id="e4b49-120">Orientation</span></span> | <span data-ttu-id="e4b49-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4b49-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b49-122">Paisagem</span><span class="sxs-lookup"><span data-stu-id="e4b49-122">Landscape</span></span>   | <span data-ttu-id="e4b49-123">A largura da capa é maior que a altura da capa.</span><span class="sxs-lookup"><span data-stu-id="e4b49-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="e4b49-124">A exibição é orientada de maneira horizontal.</span><span class="sxs-lookup"><span data-stu-id="e4b49-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="e4b49-125">Retrato</span><span class="sxs-lookup"><span data-stu-id="e4b49-125">Portrait</span></span>    | <span data-ttu-id="e4b49-126">A altura da capa é maior que a largura da capa.</span><span class="sxs-lookup"><span data-stu-id="e4b49-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="e4b49-127">A exibição é orientada em uma maneira vertical.</span><span class="sxs-lookup"><span data-stu-id="e4b49-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="e4b49-128">Square</span><span class="sxs-lookup"><span data-stu-id="e4b49-128">Square</span></span>      | <span data-ttu-id="e4b49-129">A altura da capa é igual à largura da capa.</span><span class="sxs-lookup"><span data-stu-id="e4b49-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="e4b49-130">A exibição não tem orientação.</span><span class="sxs-lookup"><span data-stu-id="e4b49-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="e4b49-131">O Windows Media Player 9 Series para Windows Mobile 2003 exibirá apenas uma determinada capa quando a seção de descrição especificada no arquivo de definição de capa corresponder ao estado atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4b49-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="e4b49-132">Você deve ter cuidado para sempre especificar as dimensões, a resolução e a orientação corretas para as quais sua capa foi criada.</span><span class="sxs-lookup"><span data-stu-id="e4b49-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="e4b49-133">Por exemplo, se as dimensões especificadas pela sua capa descreverem uma orientação paisagem, sua capa não estará disponível quando o dispositivo estiver no modo retrato, mesmo se você especificar retrato na linha de orientação.</span><span class="sxs-lookup"><span data-stu-id="e4b49-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4b49-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4b49-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b49-135">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="e4b49-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




