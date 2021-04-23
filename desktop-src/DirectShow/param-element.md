---
description: O elemento param especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909034"
---
# <a name="param-element"></a><span data-ttu-id="47122-103">Elemento param</span><span class="sxs-lookup"><span data-stu-id="47122-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="47122-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="47122-104">\[Deprecated.</span></span> <span data-ttu-id="47122-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="47122-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="47122-106">O `param` elemento Especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.</span><span class="sxs-lookup"><span data-stu-id="47122-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="47122-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="47122-107">Attributes</span></span>

<span data-ttu-id="47122-108">[**nome**](name-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="47122-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="47122-109">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="47122-109">Parent/Child Information</span></span>



| <span data-ttu-id="47122-110">Label</span><span class="sxs-lookup"><span data-stu-id="47122-110">Label</span></span> | <span data-ttu-id="47122-111">Valor</span><span class="sxs-lookup"><span data-stu-id="47122-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47122-112">Pai</span><span class="sxs-lookup"><span data-stu-id="47122-112">Parent</span></span>   | <span data-ttu-id="47122-113">[**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="47122-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="47122-114">Children</span><span class="sxs-lookup"><span data-stu-id="47122-114">Children</span></span> | <span data-ttu-id="47122-115">[**em**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="47122-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="47122-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="47122-116">Remarks</span></span>

<span data-ttu-id="47122-117">O atributo **Value** especifica o valor da propriedade no início da transição ou efeito.</span><span class="sxs-lookup"><span data-stu-id="47122-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="47122-118">Use o elemento **at** ou **linear** para especificar valores de alteração.</span><span class="sxs-lookup"><span data-stu-id="47122-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="47122-119">Se o elemento **param** não contiver elementos **at** ou **lineares** , o valor permanecerá constante ao longo da duração do efeito ou da transição.</span><span class="sxs-lookup"><span data-stu-id="47122-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="47122-120">Um elemento **param** dentro de um elemento **clip** não pode conter elementos **at** ou **lineares** .</span><span class="sxs-lookup"><span data-stu-id="47122-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="47122-121">Muitas transições dão suporte a uma propriedade de **progresso** padrão que varia de 0 a 1,0, indicando qual porcentagem da transição é refletida na saída.</span><span class="sxs-lookup"><span data-stu-id="47122-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="47122-122">Em **andamento** = 0,0, a transição está no início de sua sequência (totalmente a primeira imagem de vídeo).</span><span class="sxs-lookup"><span data-stu-id="47122-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="47122-123">Em **andamento** = 0,5, a transição é a metade concluída.</span><span class="sxs-lookup"><span data-stu-id="47122-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="47122-124">(Por exemplo, em um apagamento, em **andamento** = 0,5, o limite de transição está no centro da imagem) Em **andamento** = 1,0, a transição é concluída (totalmente a segunda imagem).</span><span class="sxs-lookup"><span data-stu-id="47122-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="47122-125">Por padrão, as transições vão de **Progress** = 0,0 no início da transição para **Progress** = 1,0 no final.</span><span class="sxs-lookup"><span data-stu-id="47122-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="47122-126">Outras propriedades geralmente são específicas para uma transição ou efeito específico.</span><span class="sxs-lookup"><span data-stu-id="47122-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="47122-127">Por exemplo, a transição de apagamento dá suporte a uma propriedade **GradientSize** que controla a largura da área de transição.</span><span class="sxs-lookup"><span data-stu-id="47122-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="47122-128">Para executar uma transição para trás, defina a propriedade **Progress** como 1,0 no início da transição e use o elemento **linear** para alterar o valor para 0,0, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="47122-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="47122-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47122-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="47122-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="47122-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47122-131">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="47122-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



