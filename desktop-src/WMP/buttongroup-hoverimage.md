---
title: BUTTON. hoverImage
description: O atributo hoverImage especifica ou recupera o nome da imagem que representa o estado de foco de um botão no botão. O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- HoverImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770517"
---
# <a name="buttongrouphoverimage"></a><span data-ttu-id="230e6-105">BUTTON. hoverImage</span><span class="sxs-lookup"><span data-stu-id="230e6-105">BUTTONGROUP.hoverImage</span></span>

<span data-ttu-id="230e6-106">O atributo **hoverImage** especifica ou recupera o nome da imagem que representa o estado de foco de um botão no **botão**.</span><span class="sxs-lookup"><span data-stu-id="230e6-106">The **hoverImage** attribute specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="230e6-107">O estado de foco ocorre quando o botão está no estado ativo e o usuário passa o mouse sobre ele.</span><span class="sxs-lookup"><span data-stu-id="230e6-107">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="230e6-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="230e6-108">Possible Values</span></span>

<span data-ttu-id="230e6-109">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="230e6-109">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="230e6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="230e6-110">Remarks</span></span>

<span data-ttu-id="230e6-111">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="230e6-111">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="230e6-112">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .</span><span class="sxs-lookup"><span data-stu-id="230e6-112">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="230e6-113">A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.</span><span class="sxs-lookup"><span data-stu-id="230e6-113">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="230e6-114">Se a imagem em foco for maior que a região definida, a imagem em foco será cortada.</span><span class="sxs-lookup"><span data-stu-id="230e6-114">If the hover image is larger than the defined region, the hover image will be cropped.</span></span>

<span data-ttu-id="230e6-115">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="230e6-115">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="230e6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="230e6-116">Examples</span></span>

<span data-ttu-id="230e6-117">Consulte o *botãoelement*. atributo [mappingColor](buttonelement-mappingcolor.md) para um exemplo que ilustra o uso desse atributo.</span><span class="sxs-lookup"><span data-stu-id="230e6-117">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="230e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230e6-118">Requirements</span></span>



| <span data-ttu-id="230e6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="230e6-119">Requirement</span></span> | <span data-ttu-id="230e6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="230e6-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="230e6-121">Versão</span><span class="sxs-lookup"><span data-stu-id="230e6-121">Version</span></span><br/> | <span data-ttu-id="230e6-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="230e6-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="230e6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="230e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230e6-124">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="230e6-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="230e6-125">**BUTTON. hueShift**</span><span class="sxs-lookup"><span data-stu-id="230e6-125">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="230e6-126">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="230e6-126">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="230e6-127">**BOTÃO. saturação**</span><span class="sxs-lookup"><span data-stu-id="230e6-127">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





