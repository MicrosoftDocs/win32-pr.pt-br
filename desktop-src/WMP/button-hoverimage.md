---
title: BUTTON. hoverImage
description: O atributo hoverImage especifica ou recupera a imagem exibida quando o botão está no estado ativo e o usuário passa sobre ele com o ponteiro do mouse.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781275"
---
# <a name="buttonhoverimage"></a><span data-ttu-id="3aa92-104">BUTTON. hoverImage</span><span class="sxs-lookup"><span data-stu-id="3aa92-104">BUTTON.hoverImage</span></span>

<span data-ttu-id="3aa92-105">O atributo **hoverImage** especifica ou recupera a imagem exibida quando o **botão** está no estado ativo e o usuário passa sobre ele com o ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="3aa92-105">The **hoverImage** attribute specifies or retrieves the image displayed when the **BUTTON** is in the up state and the user hovers over it with the mouse pointer.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="3aa92-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3aa92-106">Possible Values</span></span>

<span data-ttu-id="3aa92-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="3aa92-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa92-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aa92-108">Remarks</span></span>

<span data-ttu-id="3aa92-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="3aa92-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="3aa92-110">A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.</span><span class="sxs-lookup"><span data-stu-id="3aa92-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="3aa92-111">Se a imagem em foco for maior do que a região definida no atributo ambiente, a imagem em foco será cortada.</span><span class="sxs-lookup"><span data-stu-id="3aa92-111">If the hover image is larger than the defined region in the ambient attribute, the hover image will be cropped.</span></span>

<span data-ttu-id="3aa92-112">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="3aa92-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa92-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa92-113">Requirements</span></span>



| <span data-ttu-id="3aa92-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa92-114">Requirement</span></span> | <span data-ttu-id="3aa92-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3aa92-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3aa92-116">Versão</span><span class="sxs-lookup"><span data-stu-id="3aa92-116">Version</span></span><br/> | <span data-ttu-id="3aa92-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3aa92-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3aa92-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aa92-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa92-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="3aa92-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="3aa92-120">**BOTÃO. imagem**</span><span class="sxs-lookup"><span data-stu-id="3aa92-120">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





