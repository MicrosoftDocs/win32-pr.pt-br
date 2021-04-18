---
title: BUTTON. transparencyColor
description: O atributo transparencyColor especifica ou recupera a cor que será transparente nas imagens de botão.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784910"
---
# <a name="buttontransparencycolor"></a><span data-ttu-id="4974c-104">BUTTON. transparencyColor</span><span class="sxs-lookup"><span data-stu-id="4974c-104">BUTTON.transparencyColor</span></span>

<span data-ttu-id="4974c-105">O atributo **transparencyColor** especifica ou recupera a cor que será transparente nas imagens de **botão** .</span><span class="sxs-lookup"><span data-stu-id="4974c-105">The **transparencyColor** attribute specifies or retrieves the color that will be transparent in the **BUTTON** images.</span></span>

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a><span data-ttu-id="4974c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4974c-106">Possible Values</span></span>

<span data-ttu-id="4974c-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação sem padrão contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4974c-107">This attribute is a read/write **String** with no default containing one of the following values.</span></span>



| <span data-ttu-id="4974c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4974c-108">Value</span></span>                                    | <span data-ttu-id="4974c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4974c-109">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4974c-110">Automático</span><span class="sxs-lookup"><span data-stu-id="4974c-110">Auto</span></span>                                     | <span data-ttu-id="4974c-111">A cor do pixel no local 0, 0 na imagem torna-se a cor transparente.</span><span class="sxs-lookup"><span data-stu-id="4974c-111">The color of the pixel at location 0,0 in the image becomes the transparent color.</span></span>                        |
| <span data-ttu-id="4974c-112">Qualquer valor de formato de cor do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4974c-112">Any Internet Explorer color format value</span></span> | <span data-ttu-id="4974c-113">Um valor de formato de cor do Internet Explorer se torna a cor transparente (por exemplo, "vermelho" ou " \# FF0000").</span><span class="sxs-lookup"><span data-stu-id="4974c-113">An Internet Explorer color format value becomes the transparent color (for example, "red" or "\#FF0000").</span></span> |
| <span data-ttu-id="4974c-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4974c-114">None</span></span>                                     | <span data-ttu-id="4974c-115">Sem transparência.</span><span class="sxs-lookup"><span data-stu-id="4974c-115">No transparency.</span></span>                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="4974c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4974c-116">Remarks</span></span>

<span data-ttu-id="4974c-117">Uma cor transparente em uma imagem permite que tudo esteja atrás da imagem para mostrar as áreas transparentes.</span><span class="sxs-lookup"><span data-stu-id="4974c-117">A transparent color in an image allows whatever is behind the image to show through the transparent areas.</span></span> <span data-ttu-id="4974c-118">O **botão** ainda receberá cliques na região transparente.</span><span class="sxs-lookup"><span data-stu-id="4974c-118">The **BUTTON** will still receive clicks on the transparent region.</span></span>

<span data-ttu-id="4974c-119">A cor transparente pode ser qualquer valor de cor do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4974c-119">The transparent color can be any Internet Explorer color value.</span></span> <span data-ttu-id="4974c-120">Se o valor do atributo **transparencyColor** for definido como "auto", a cor do pixel no local 0, 0 na imagem, será usada.</span><span class="sxs-lookup"><span data-stu-id="4974c-120">If the value of the **transparencyColor** attribute is set to "Auto", the color of the pixel at location 0,0 in the image is used.</span></span>

<span data-ttu-id="4974c-121">Se a cor especificada não for uma das cores válidas do IE, o valor anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="4974c-121">If the color specified is not one of the valid IE colors, the previous value is maintained.</span></span>

<span data-ttu-id="4974c-122">Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados quando **transparencyColor** é usado.</span><span class="sxs-lookup"><span data-stu-id="4974c-122">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended when **transparencyColor** is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4974c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4974c-123">Requirements</span></span>



| <span data-ttu-id="4974c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4974c-124">Requirement</span></span> | <span data-ttu-id="4974c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4974c-125">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4974c-126">Versão</span><span class="sxs-lookup"><span data-stu-id="4974c-126">Version</span></span><br/> | <span data-ttu-id="4974c-127">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4974c-127">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4974c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4974c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4974c-129">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="4974c-129">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="4974c-130">**BOTÃO. imagem**</span><span class="sxs-lookup"><span data-stu-id="4974c-130">**BUTTON.image**</span></span>](button-image.md)
</dt> <dt>

[<span data-ttu-id="4974c-131">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="4974c-131">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





