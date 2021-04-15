---
title: SLIDER. foregroundColor
description: O atributo foregroundColor especifica ou recupera a cor de primeiro plano do controle deslizante.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Controle deslizante. foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753886"
---
# <a name="sliderforegroundcolor"></a><span data-ttu-id="06e21-104">SLIDER. foregroundColor</span><span class="sxs-lookup"><span data-stu-id="06e21-104">SLIDER.foregroundColor</span></span>

<span data-ttu-id="06e21-105">O atributo **foregroundColor** especifica ou recupera a cor de primeiro plano do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="06e21-105">The **foregroundColor** attribute specifies or retrieves the foreground color of the slider control.</span></span>

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a><span data-ttu-id="06e21-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="06e21-106">Possible Values</span></span>

<span data-ttu-id="06e21-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém qualquer valor de cor do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="06e21-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="06e21-108">O valor padrão é "White".</span><span class="sxs-lookup"><span data-stu-id="06e21-108">The default value is "white".</span></span>

## <a name="remarks"></a><span data-ttu-id="06e21-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="06e21-109">Remarks</span></span>

<span data-ttu-id="06e21-110">Um controle Slider básico pode ser construído especificando um dos dois pares de atributos: **backgroundColor** e **ForegroundColor**, ou **backgroundImage** e **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="06e21-110">A basic slider control can be constructed by specifying one of two pairs of attributes: the **backgroundColor** and **foregroundColor**, or the **backgroundImage** and **foregroundImage**.</span></span>

<span data-ttu-id="06e21-111">Quando você constrói um controle deslizante usando os atributos de cor, as dimensões do controle deslizante definem a área preenchida pela cor da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="06e21-111">When you construct a slider control using the color attributes, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="06e21-112">A cor do primeiro plano cobre a cor do plano de fundo conforme a posição do controle deslizante aumenta.</span><span class="sxs-lookup"><span data-stu-id="06e21-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="06e21-113">Para fazer um preenchimento gradual na área ocupada pelo plano de fundo ou pela cor de primeiro plano, especifique os atributos **backgroundEndColor** ou **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="06e21-113">To make a gradient fill in the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="06e21-114">Consulte o *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para um exemplo que ilustra como os atributos do elemento **Slider** são usados.</span><span class="sxs-lookup"><span data-stu-id="06e21-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e21-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06e21-115">Requirements</span></span>



| <span data-ttu-id="06e21-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06e21-116">Requirement</span></span> | <span data-ttu-id="06e21-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06e21-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="06e21-118">Versão</span><span class="sxs-lookup"><span data-stu-id="06e21-118">Version</span></span><br/> | <span data-ttu-id="06e21-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="06e21-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06e21-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="06e21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e21-121">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="06e21-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="06e21-122">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="06e21-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="06e21-123">**SLIDER. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="06e21-123">**SLIDER.backgroundColor**</span></span>](slider-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="06e21-124">**SLIDER. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="06e21-124">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="06e21-125">**SLIDER. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="06e21-125">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="06e21-126">**SLIDER. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="06e21-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





