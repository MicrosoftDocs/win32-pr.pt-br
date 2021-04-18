---
title: BUTTON. mappingImage
description: O atributo mappingImage especifica ou recupera o nome da imagem que representa o mapa de botão do botão.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- MappingImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760277"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="7df3d-104">BUTTON. mappingImage</span><span class="sxs-lookup"><span data-stu-id="7df3d-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="7df3d-105">O atributo **mappingImage** especifica ou recupera o nome da imagem que representa o mapa de botão do **botão**.</span><span class="sxs-lookup"><span data-stu-id="7df3d-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="7df3d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7df3d-106">Possible Values</span></span>

<span data-ttu-id="7df3d-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7df3d-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df3d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df3d-108">Remarks</span></span>

<span data-ttu-id="7df3d-109">Este é um atributo obrigatório que deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="7df3d-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="7df3d-110">A imagem de mapeamento deve ter as mesmas dimensões que a **imagem** principal.</span><span class="sxs-lookup"><span data-stu-id="7df3d-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="7df3d-111">É um mapa das áreas clicáveis da imagem principal.</span><span class="sxs-lookup"><span data-stu-id="7df3d-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="7df3d-112">Construa o mapa preenchendo cada área clicável com uma cor diferente.</span><span class="sxs-lookup"><span data-stu-id="7df3d-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="7df3d-113">Ao definir cada **buttonelement**, designe sua cor a partir do mapa usando o atributo **mappingColor** .</span><span class="sxs-lookup"><span data-stu-id="7df3d-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="7df3d-114">Por exemplo, se você tiver um gráfico de botão de sinal de parada na imagem principal, poderá criar um mapa com a área do sinal vermelho.</span><span class="sxs-lookup"><span data-stu-id="7df3d-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="7df3d-115">O atributo **buttonelement** deve ser especificado como vermelho para tornar a imagem de parada-assinatura clicável.</span><span class="sxs-lookup"><span data-stu-id="7df3d-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="7df3d-116">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="7df3d-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="7df3d-117">Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados para mapear imagens.</span><span class="sxs-lookup"><span data-stu-id="7df3d-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="7df3d-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7df3d-118">Examples</span></span>

<span data-ttu-id="7df3d-119">A ilustração a seguir é um exemplo de um **mappingImage** e a imagem visível à qual ele corresponde.</span><span class="sxs-lookup"><span data-stu-id="7df3d-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="7df3d-120">Essas imagens fazem parte da capa na pequena pasta incluída no SDK.</span><span class="sxs-lookup"><span data-stu-id="7df3d-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![exemplo de imagem de mapeamento](images/absam01m.png)![imagem de plano de fundo de exemplo](images/absam01f.png)

<span data-ttu-id="7df3d-123">Consulte o *botãoelement*. atributo [mappingColor](buttonelement-mappingcolor.md) para um exemplo de código que ilustra o uso desse atributo.</span><span class="sxs-lookup"><span data-stu-id="7df3d-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7df3d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df3d-124">Requirements</span></span>



| <span data-ttu-id="7df3d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df3d-125">Requirement</span></span> | <span data-ttu-id="7df3d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7df3d-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7df3d-127">Versão</span><span class="sxs-lookup"><span data-stu-id="7df3d-127">Version</span></span><br/> | <span data-ttu-id="7df3d-128">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7df3d-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7df3d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df3d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df3d-130">**BUTTONelement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="7df3d-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="7df3d-131">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="7df3d-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="7df3d-132">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="7df3d-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="7df3d-133">**BUTTON. transparencyColor**</span><span class="sxs-lookup"><span data-stu-id="7df3d-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





