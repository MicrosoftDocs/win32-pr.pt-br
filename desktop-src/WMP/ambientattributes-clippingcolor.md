---
title: Ambienteattributes. clippingColor
description: O atributo clippingColor especifica ou recupera a cor a ser recortada do bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- ClippingColor do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762112"
---
# <a name="ambientattributesclippingcolor"></a><span data-ttu-id="6d8ac-104">Ambienteattributes. clippingColor</span><span class="sxs-lookup"><span data-stu-id="6d8ac-104">AmbientAttributes.clippingColor</span></span>

<span data-ttu-id="6d8ac-105">O atributo **clippingColor** especifica ou recupera a cor a ser recortada do bitmap **clippingImage** .</span><span class="sxs-lookup"><span data-stu-id="6d8ac-105">The **clippingColor** attribute specifies or retrieves the color to clip out from the **clippingImage** bitmap.</span></span>

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a><span data-ttu-id="6d8ac-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6d8ac-106">Possible Values</span></span>

<span data-ttu-id="6d8ac-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="6d8ac-108">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8ac-108">Value</span></span>                                       | <span data-ttu-id="6d8ac-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d8ac-109">Description</span></span>                                       |
|---------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6d8ac-110">Automático</span><span class="sxs-lookup"><span data-stu-id="6d8ac-110">Auto</span></span>                                        | <span data-ttu-id="6d8ac-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-111">Default.</span></span> <span data-ttu-id="6d8ac-112">A cor no local do pixel 0, 0 é usada.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-112">The color at pixel location 0,0 is used.</span></span> |
| <span data-ttu-id="6d8ac-113">qualquer valor de cor do Microsoft Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="6d8ac-113">any Microsoft Internet Explorer color value</span></span> | <span data-ttu-id="6d8ac-114">A cor especificada do Internet Explorer é usada.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-114">The specified Internet Explorer color is used.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="6d8ac-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d8ac-115">Remarks</span></span>

<span data-ttu-id="6d8ac-116">A cor de recorte indica as regiões do **clippingImage** (ou **backgroundImage** para **exibição** ou **subexibição**) que correspondem às partes transparentes e não clicáveis do controle.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-116">The clipping color indicates the regions of the **clippingImage** (or **backgroundImage** for **VIEW** or **SUBVIEW**) that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="6d8ac-117">A cor de recorte pode indicar várias regiões a serem recortadas. Um aviso será emitido se o **clippingImage** for um jpg para avisar sobre a perda de cor em JPGs.</span><span class="sxs-lookup"><span data-stu-id="6d8ac-117">The clipping color can indicate multiple regions to be clipped out. A warning is issued if the **clippingImage** is a JPG to warn of loss of color in JPGs.</span></span>

<span data-ttu-id="6d8ac-118">O atributo **clippingColor** não é suportado pelo elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="6d8ac-118">The **clippingColor** attribute is not supported by the **PLAYLIST** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8ac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8ac-119">Requirements</span></span>



| <span data-ttu-id="6d8ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8ac-120">Requirement</span></span> | <span data-ttu-id="6d8ac-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6d8ac-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6d8ac-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6d8ac-122">Version</span></span><br/> | <span data-ttu-id="6d8ac-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6d8ac-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d8ac-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d8ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8ac-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="6d8ac-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d8ac-126">**Ambienteattributes. clippingImage**</span><span class="sxs-lookup"><span data-stu-id="6d8ac-126">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> <dt>

[<span data-ttu-id="6d8ac-127">**Referência de cor**</span><span class="sxs-lookup"><span data-stu-id="6d8ac-127">**Color Reference**</span></span>](color-reference.md)
</dt> </dl>

 

 





