---
title: BUTTON. transparencyColor
description: O atributo transparencyColor especifica ou recupera a cor transparente das imagens de um botão.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- TransparencyColor Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794505"
---
# <a name="buttongrouptransparencycolor"></a><span data-ttu-id="b6ad0-104">BUTTON. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="b6ad0-104">BUTTONGROUP.transparencyColor</span></span>

<span data-ttu-id="b6ad0-105">O atributo **transparencyColor** especifica ou recupera a cor transparente das imagens de um **botão** .</span><span class="sxs-lookup"><span data-stu-id="b6ad0-105">The **transparencyColor** attribute specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="b6ad0-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b6ad0-106">Possible Values</span></span>

<span data-ttu-id="b6ad0-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação sem padrão, contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-107">This attribute is a read/write **String** with no default, containing one of the following values.</span></span>



| <span data-ttu-id="b6ad0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b6ad0-108">Value</span></span>                                       | <span data-ttu-id="b6ad0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6ad0-109">Description</span></span>                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ad0-110">Automático</span><span class="sxs-lookup"><span data-stu-id="b6ad0-110">Auto</span></span>                                        | <span data-ttu-id="b6ad0-111">O pixel no local 0, 0 na imagem torna-se a cor transparente.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-111">The pixel at location 0,0 in the image becomes the transparent color.</span></span>                              |
| <span data-ttu-id="b6ad0-112">qualquer valor de cor do Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b6ad0-112">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="b6ad0-113">Um valor de cor do Internet Explorer se torna a cor transparente (por exemplo, "vermelho" ou " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="b6ad0-113">An Internet Explorer color value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="b6ad0-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6ad0-114">None</span></span>                                        | <span data-ttu-id="b6ad0-115">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-115">Default.</span></span> <span data-ttu-id="b6ad0-116">Sem transparência.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-116">No transparency.</span></span>                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="b6ad0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6ad0-117">Remarks</span></span>

<span data-ttu-id="b6ad0-118">Uma cor transparente em uma imagem permitirá que tudo esteja atrás da imagem para mostrar as áreas de transparência.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-118">A transparent color in an image will allow whatever is behind the image to show through the areas of transparency.</span></span> <span data-ttu-id="b6ad0-119">A região transparente é clicável, a menos que recortada pela marca **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="b6ad0-119">The transparent region is clickable unless clipped by the **clippingImage** tag.</span></span>

<span data-ttu-id="b6ad0-120">A cor pode ser qualquer valor de cor do Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-120">The color can be any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="b6ad0-121">Se o valor for auto, a cor do pixel no local 0, 0 na imagem, será usada.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-121">If the value is Auto, then the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="b6ad0-122">Se a cor especificada não for uma das cores válidas do Internet Explorer, um aviso será retornado e o valor anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-122">If the color specified is not one of the valid Internet Explorer colors, a warning is returned and the previous value is maintained.</span></span>

<span data-ttu-id="b6ad0-123">Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados quando **transparencyColor** é usado.</span><span class="sxs-lookup"><span data-stu-id="b6ad0-123">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ad0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ad0-124">Requirements</span></span>



| <span data-ttu-id="b6ad0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ad0-125">Requirement</span></span> | <span data-ttu-id="b6ad0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b6ad0-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b6ad0-127">Versão</span><span class="sxs-lookup"><span data-stu-id="b6ad0-127">Version</span></span><br/> | <span data-ttu-id="b6ad0-128">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b6ad0-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6ad0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6ad0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ad0-130">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="b6ad0-130">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="b6ad0-131">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="b6ad0-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





