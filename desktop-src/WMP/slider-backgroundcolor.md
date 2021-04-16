---
title: SLIDER. backgroundColor
description: O atributo backgroundColor especifica ou recupera a cor do plano de fundo do controle deslizante.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Controle deslizante. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753675"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="66451-104">SLIDER. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="66451-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="66451-105">O atributo **backgroundColor** especifica ou recupera a cor do plano de fundo do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="66451-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="66451-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="66451-106">Possible Values</span></span>

<span data-ttu-id="66451-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="66451-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="66451-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="66451-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66451-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="66451-109">Remarks</span></span>

<span data-ttu-id="66451-110">Um controle Slider básico pode ser construído especificando **backgroundColor** ou **BackgroundImage**, e **foregroundColor** ou **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="66451-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="66451-111">Ao usar as cores, as dimensões do controle deslizante definem a área preenchida pela cor da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="66451-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="66451-112">A cor do primeiro plano cobre a cor do plano de fundo conforme a posição do controle deslizante aumenta.</span><span class="sxs-lookup"><span data-stu-id="66451-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="66451-113">Para fazer um preenchimento gradual da área ocupada pela cor do plano de fundo ou do primeiro plano, especifique os atributos **backgroundEndColor** ou **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="66451-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="66451-114">Consulte o *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.</span><span class="sxs-lookup"><span data-stu-id="66451-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="66451-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66451-115">Requirements</span></span>



| <span data-ttu-id="66451-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66451-116">Requirement</span></span> | <span data-ttu-id="66451-117">Valor</span><span class="sxs-lookup"><span data-stu-id="66451-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="66451-118">Versão</span><span class="sxs-lookup"><span data-stu-id="66451-118">Version</span></span><br/> | <span data-ttu-id="66451-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="66451-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66451-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="66451-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66451-121">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="66451-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="66451-122">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="66451-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="66451-123">**SLIDER. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="66451-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="66451-124">**SLIDER. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="66451-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="66451-125">**SLIDER. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="66451-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="66451-126">**SLIDER. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="66451-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="66451-127">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="66451-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





