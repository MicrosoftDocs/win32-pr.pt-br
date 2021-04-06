---
description: O elemento param especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825901"
---
# <a name="param-element"></a><span data-ttu-id="a432a-103">Elemento param</span><span class="sxs-lookup"><span data-stu-id="a432a-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="a432a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a432a-104">\[Deprecated.</span></span> <span data-ttu-id="a432a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a432a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a432a-106">O `param` elemento Especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.</span><span class="sxs-lookup"><span data-stu-id="a432a-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="a432a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a432a-107">Attributes</span></span>

<span data-ttu-id="a432a-108">[**nome**](name-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="a432a-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="a432a-109">Informações de pai/filho</span><span class="sxs-lookup"><span data-stu-id="a432a-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a432a-110">Pai</span><span class="sxs-lookup"><span data-stu-id="a432a-110">Parent</span></span>   | <span data-ttu-id="a432a-111">[**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="a432a-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="a432a-112">Children</span><span class="sxs-lookup"><span data-stu-id="a432a-112">Children</span></span> | <span data-ttu-id="a432a-113">[**em**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="a432a-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="a432a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a432a-114">Remarks</span></span>

<span data-ttu-id="a432a-115">O atributo **Value** especifica o valor da propriedade no início da transição ou efeito.</span><span class="sxs-lookup"><span data-stu-id="a432a-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="a432a-116">Use o elemento **at** ou **linear** para especificar valores de alteração.</span><span class="sxs-lookup"><span data-stu-id="a432a-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="a432a-117">Se o elemento **param** não contiver elementos **at** ou **lineares** , o valor permanecerá constante ao longo da duração do efeito ou da transição.</span><span class="sxs-lookup"><span data-stu-id="a432a-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="a432a-118">Um elemento **param** dentro de um elemento **clip** não pode conter elementos **at** ou **lineares** .</span><span class="sxs-lookup"><span data-stu-id="a432a-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="a432a-119">Muitas transições dão suporte a uma propriedade de **progresso** padrão que varia de 0 a 1,0, indicando qual porcentagem da transição é refletida na saída.</span><span class="sxs-lookup"><span data-stu-id="a432a-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="a432a-120">Em **andamento** = 0,0, a transição está no início de sua sequência (totalmente a primeira imagem de vídeo).</span><span class="sxs-lookup"><span data-stu-id="a432a-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="a432a-121">Em **andamento** = 0,5, a transição é a metade concluída.</span><span class="sxs-lookup"><span data-stu-id="a432a-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="a432a-122">(Por exemplo, em um apagamento, em **andamento** = 0,5, o limite de transição está no centro da imagem) Em **andamento** = 1,0, a transição é concluída (totalmente a segunda imagem).</span><span class="sxs-lookup"><span data-stu-id="a432a-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="a432a-123">Por padrão, as transições vão de **Progress** = 0,0 no início da transição para **Progress** = 1,0 no final.</span><span class="sxs-lookup"><span data-stu-id="a432a-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="a432a-124">Outras propriedades geralmente são específicas para uma transição ou efeito específico.</span><span class="sxs-lookup"><span data-stu-id="a432a-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="a432a-125">Por exemplo, a transição de apagamento dá suporte a uma propriedade **GradientSize** que controla a largura da área de transição.</span><span class="sxs-lookup"><span data-stu-id="a432a-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="a432a-126">Para executar uma transição para trás, defina a propriedade **Progress** como 1,0 no início da transição e use o elemento **linear** para alterar o valor para 0,0, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a432a-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="a432a-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a432a-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="a432a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a432a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a432a-129">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="a432a-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



