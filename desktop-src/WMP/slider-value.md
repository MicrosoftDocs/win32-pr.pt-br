---
title: Controle deslizante. valor
description: O atributo Value especifica ou recupera a posição atual do controle deslizante. | Controle deslizante. valor
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Controle deslizante. valor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751031"
---
# <a name="slidervalue"></a><span data-ttu-id="94a34-105">Controle deslizante. valor</span><span class="sxs-lookup"><span data-stu-id="94a34-105">SLIDER.value</span></span>

<span data-ttu-id="94a34-106">O atributo **Value** especifica ou recupera a posição atual do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="94a34-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="94a34-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="94a34-107">Possible Values</span></span>

<span data-ttu-id="94a34-108">Esse atributo é um **número** de leitura/gravação (**float**) com um valor padrão de **mín**.</span><span class="sxs-lookup"><span data-stu-id="94a34-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="94a34-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="94a34-109">Remarks</span></span>

<span data-ttu-id="94a34-110">O **valor** deve ser sempre maior ou igual a **mín** e menor ou igual ao **máximo**. Se você especificar um valor fora desse intervalo, o **valor** e a posição do controle deslizante não serão alterados.</span><span class="sxs-lookup"><span data-stu-id="94a34-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="94a34-111">Consulte o **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.</span><span class="sxs-lookup"><span data-stu-id="94a34-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="94a34-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94a34-112">Requirements</span></span>



| <span data-ttu-id="94a34-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="94a34-113">Requirement</span></span> | <span data-ttu-id="94a34-114">Valor</span><span class="sxs-lookup"><span data-stu-id="94a34-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="94a34-115">Versão</span><span class="sxs-lookup"><span data-stu-id="94a34-115">Version</span></span><br/> | <span data-ttu-id="94a34-116">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="94a34-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94a34-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="94a34-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a34-118">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="94a34-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="94a34-119">**SLIDER. min**</span><span class="sxs-lookup"><span data-stu-id="94a34-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





