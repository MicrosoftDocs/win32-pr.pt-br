---
title: BUTTON. hoverDownImage
description: O atributo hoverDownImage especifica ou recupera a imagem exibida quando o botão está no estado inoperante e o usuário passa sobre ele com o ponteiro do mouse.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760893"
---
# <a name="buttonhoverdownimage"></a><span data-ttu-id="a9258-104">BUTTON. hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="a9258-104">BUTTON.hoverDownImage</span></span>

<span data-ttu-id="a9258-105">O atributo **hoverDownImage** especifica ou recupera a imagem exibida quando o **botão** está no estado inoperante e o usuário passa sobre ele com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="a9258-105">The **hoverDownImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the down state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a><span data-ttu-id="a9258-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a9258-106">Possible Values</span></span>

<span data-ttu-id="a9258-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="a9258-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9258-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9258-108">Remarks</span></span>

<span data-ttu-id="a9258-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="a9258-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="a9258-110">A imagem padrão é aquela especificada no atributo **downImage** ou seu padrão.</span><span class="sxs-lookup"><span data-stu-id="a9258-110">The default image is the one specified in the **downImage** attribute, or its default.</span></span>

<span data-ttu-id="a9258-111">Se a imagem focalizada for maior do que a região definida no atributo ambiente, a imagem focalizada será cortada.</span><span class="sxs-lookup"><span data-stu-id="a9258-111">If the hover-down image is larger than the defined region in the ambient attribute, the hover-down image will be cropped.</span></span>

<span data-ttu-id="a9258-112">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="a9258-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9258-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9258-113">Requirements</span></span>



| <span data-ttu-id="a9258-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9258-114">Requirement</span></span> | <span data-ttu-id="a9258-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a9258-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a9258-116">Versão</span><span class="sxs-lookup"><span data-stu-id="a9258-116">Version</span></span><br/> | <span data-ttu-id="a9258-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a9258-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9258-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9258-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9258-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="a9258-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="a9258-120">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="a9258-120">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





