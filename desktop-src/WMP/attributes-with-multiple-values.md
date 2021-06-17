---
title: Atributos com vários valores (SDK do Windows Media Player)
description: Saiba mais sobre atributos com vários valores no SDK do Windows Media Player. Alguns atributos de item de mídia podem ter vários valores.
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
ms.openlocfilehash: a16baf4bab47dc972ec7b043980dccb0f2aadd57
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262598"
---
# <a name="attributes-with-multiple-values-windows-media-player-sdk"></a><span data-ttu-id="22aed-115">Atributos com vários valores (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="22aed-115">Attributes with Multiple Values (Windows Media Player SDK)</span></span>

<span data-ttu-id="22aed-116">Alguns atributos de item de mídia podem ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="22aed-116">Some media item attributes can have multiple values.</span></span> <span data-ttu-id="22aed-117">Por exemplo, os atributos **autor**, **WM/Composer** e **WM/gênero** podem ter mais de um valor.</span><span class="sxs-lookup"><span data-stu-id="22aed-117">For example, the **Author**, **WM/Composer**, and **WM/Genre** attributes can each have more than one value.</span></span> <span data-ttu-id="22aed-118">O tipo de dados desses atributos é uma **cadeia de caracteres com valores múltiplos**.</span><span class="sxs-lookup"><span data-stu-id="22aed-118">The data type of such attributes is **multi-valued string**.</span></span>

<span data-ttu-id="22aed-119">No Windows Media Player, a biblioteca exibe vários valores em um único campo, separando os valores com ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="22aed-119">In Windows Media Player, the library displays multiple values in a single field, separating the values with semicolons.</span></span> <span data-ttu-id="22aed-120">No entanto, cada valor é, na verdade, um atributo separado no item Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22aed-120">However, each value is actually a separate attribute in the Windows Media item.</span></span>

<span data-ttu-id="22aed-121">Você pode escrever um código que determinará se um determinado atributo tem vários valores e, em seguida, recuperar todos esses valores.</span><span class="sxs-lookup"><span data-stu-id="22aed-121">You can write code that will determine whether a given attribute has multiple values and then retrieve all of those values.</span></span> <span data-ttu-id="22aed-122">Você deve usar a *mídia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="22aed-122">You must use *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="22aed-123">Se você usar a *mídia*. método **getItemInfo** para recuperar um atributo com valores múltiplos, você recuperará apenas o primeiro valor.</span><span class="sxs-lookup"><span data-stu-id="22aed-123">If you use the *Media*.**getItemInfo** method to retrieve a multi-valued attribute, you will only retrieve the first value.</span></span>

<span data-ttu-id="22aed-124">O exemplo final no tópico [valores de atributo de leitura](reading-attribute-values.md) demonstra o uso da *mídia*. **getAttributeCountByType** e *mídia*. métodos **getItemInfoByType** para recuperar vários valores para um determinado atributo.</span><span class="sxs-lookup"><span data-stu-id="22aed-124">The final example in the [Reading Attribute Values](reading-attribute-values.md) topic demonstrates the use of the *Media*.**getAttributeCountByType** and *Media*.**getItemInfoByType** methods to retrieve multiple values for a given attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22aed-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22aed-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22aed-126">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="22aed-126">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="22aed-127">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="22aed-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="22aed-128">**Lendo valores de atributo de um CD ou DVD**</span><span class="sxs-lookup"><span data-stu-id="22aed-128">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




