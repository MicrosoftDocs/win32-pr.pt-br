---
title: BUTTON. hoverDownImage
description: O atributo hoverDownImage especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no botão. O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- HoverDownImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810577"
---
# <a name="buttongrouphoverdownimage"></a><span data-ttu-id="07e5f-105">BUTTON. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="07e5f-105">BUTTONGROUP.hoverDownImage</span></span>

<span data-ttu-id="07e5f-106">O atributo **hoverDownImage** especifica ou recupera o nome da imagem que representa o estado de focalização de um botão no **botão**.</span><span class="sxs-lookup"><span data-stu-id="07e5f-106">The **hoverDownImage** attribute specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="07e5f-107">O estado de focalização ocorre quando o botão está no estado inativo e o usuário passa o mouse sobre ele.</span><span class="sxs-lookup"><span data-stu-id="07e5f-107">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="07e5f-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="07e5f-108">Possible Values</span></span>

<span data-ttu-id="07e5f-109">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="07e5f-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="07e5f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="07e5f-110">Remarks</span></span>

<span data-ttu-id="07e5f-111">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="07e5f-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="07e5f-112">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .</span><span class="sxs-lookup"><span data-stu-id="07e5f-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="07e5f-113">A imagem padrão é aquela especificada no atributo **downImage** ou seu padrão.</span><span class="sxs-lookup"><span data-stu-id="07e5f-113">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="07e5f-114">Se a imagem focalizada for maior que a região definida, a imagem focalizada será cortada.</span><span class="sxs-lookup"><span data-stu-id="07e5f-114">If the hover-down image is larger than the defined region, the hover-down image will be cropped.</span></span>

<span data-ttu-id="07e5f-115">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="07e5f-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07e5f-116">Requirements</span></span>



| <span data-ttu-id="07e5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e5f-117">Requirement</span></span> | <span data-ttu-id="07e5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="07e5f-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="07e5f-119">Versão</span><span class="sxs-lookup"><span data-stu-id="07e5f-119">Version</span></span><br/> | <span data-ttu-id="07e5f-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="07e5f-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07e5f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="07e5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e5f-122">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="07e5f-122">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="07e5f-123">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="07e5f-123">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> <dt>

[<span data-ttu-id="07e5f-124">**BUTTON. hueShift**</span><span class="sxs-lookup"><span data-stu-id="07e5f-124">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="07e5f-125">**BOTÃO. saturação**</span><span class="sxs-lookup"><span data-stu-id="07e5f-125">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





