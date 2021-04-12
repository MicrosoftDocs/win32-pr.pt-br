---
title: Atributos com vários valores (SDK do Windows Media Player)
description: Atributos com vários valores
ms.assetid: 8405481c-47f5-4752-9dab-d3c84711fbb4
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, vários valores
- vários valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad93c4025d09a234b1834a32e4ca3789bcaa4a35
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369146"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="05081-114">Atributos com vários valores (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="05081-114">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="05081-115">Alguns atributos de item de mídia podem ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="05081-115">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="05081-116">Por exemplo, os atributos **autor**, **WM/Composer** e **WM/gênero** podem ter mais de um valor.</span><span class="sxs-lookup"><span data-stu-id="05081-116">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="05081-117">O tipo de dados desses atributos é uma **cadeia de caracteres com valores múltiplos**.</span><span class="sxs-lookup"><span data-stu-id="05081-117">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="05081-118">No Windows Media Player, a biblioteca exibe vários valores em um único campo, separando os valores com ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="05081-118">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="05081-119">No entanto, cada valor é, na verdade, um atributo separado no item Windows Media.</span><span class="sxs-lookup"><span data-stu-id="05081-119">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="05081-120">Você pode escrever um código que determinará se um determinado atributo tem vários valores e, em seguida, recuperar todos esses valores.</span><span class="sxs-lookup"><span data-stu-id="05081-120">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="05081-121">Você deve usar a *mídia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="05081-121">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="05081-122">Se você usar a *mídia*. método **getItemInfo** para recuperar um atributo com valores múltiplos, você recuperará apenas o primeiro valor.</span><span class="sxs-lookup"><span data-stu-id="05081-122">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="05081-123">O exemplo final no tópico [valores de atributo de leitura](reading-attribute-values.md) demonstra o uso da *mídia*. **getAttributeCountByType** e *mídia*. métodos **getItemInfoByType** para recuperar vários valores para um determinado atributo.</span><span class="sxs-lookup"><span data-stu-id="05081-123">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05081-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05081-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05081-125">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="05081-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="05081-126">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="05081-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="05081-127">**Lendo valores de atributo de um CD ou DVD**</span><span class="sxs-lookup"><span data-stu-id="05081-127">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




