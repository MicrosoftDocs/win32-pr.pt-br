---
title: Ambienteattributes. alphaBlendTo
description: O método alphaBlendTo ajusta a propriedade alphaBlend ao longo de um período de tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AlphaBlendTo do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800172"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="0b30e-104">Ambienteattributes. alphaBlendTo</span><span class="sxs-lookup"><span data-stu-id="0b30e-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="0b30e-105">O método **alphaBlendTo** ajusta a propriedade **alphaBlend** ao longo de um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="0b30e-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="0b30e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b30e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b30e-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span><span class="sxs-lookup"><span data-stu-id="0b30e-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="0b30e-108">**Número** (longo) que especifica o novo valor de opacidade.</span><span class="sxs-lookup"><span data-stu-id="0b30e-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="0b30e-109">Varia de 0 (sem opacidade) a 255 (opacidade total).</span><span class="sxs-lookup"><span data-stu-id="0b30e-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="0b30e-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphatime*</span><span class="sxs-lookup"><span data-stu-id="0b30e-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="0b30e-111">**Número** (**longo**) que especifica o tempo, em milissegundos, que leva o elemento para alterar a opacidade.</span><span class="sxs-lookup"><span data-stu-id="0b30e-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b30e-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0b30e-112">Return Value</span></span>

<span data-ttu-id="0b30e-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0b30e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b30e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b30e-114">Remarks</span></span>

<span data-ttu-id="0b30e-115">Esse método é útil para fazer com que os elementos apareçam gradualmente ou desapareçam.</span><span class="sxs-lookup"><span data-stu-id="0b30e-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="0b30e-116">Quando você usa **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada.</span><span class="sxs-lookup"><span data-stu-id="0b30e-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="0b30e-117">Se a cor de primeiro plano também for preta (que é o valor padrão para *texto*.**foregroundColor**), seu texto pode se tornar ilegível.</span><span class="sxs-lookup"><span data-stu-id="0b30e-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="0b30e-118">Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.</span><span class="sxs-lookup"><span data-stu-id="0b30e-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="0b30e-119">Não há suporte para esse atributo no Windows 98.</span><span class="sxs-lookup"><span data-stu-id="0b30e-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0b30e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b30e-120">Requirements</span></span>



| <span data-ttu-id="0b30e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b30e-121">Requirement</span></span> | <span data-ttu-id="0b30e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0b30e-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0b30e-123">Versão</span><span class="sxs-lookup"><span data-stu-id="0b30e-123">Version</span></span><br/> | <span data-ttu-id="0b30e-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0b30e-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b30e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b30e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b30e-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="0b30e-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b30e-127">**Ambienteattributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="0b30e-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="0b30e-128">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="0b30e-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="0b30e-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="0b30e-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="0b30e-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="0b30e-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





