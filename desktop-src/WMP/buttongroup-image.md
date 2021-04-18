---
title: BUTTON. Image
description: O atributo Image especifica ou recupera o nome da imagem que representa os botões de um botão.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- MyButton. Image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760460"
---
# <a name="buttongroupimage"></a><span data-ttu-id="5a566-104">BUTTON. Image</span><span class="sxs-lookup"><span data-stu-id="5a566-104">BUTTONGROUP.image</span></span>

<span data-ttu-id="5a566-105">O atributo **Image** especifica ou recupera o nome da imagem que representa os botões de um **botão**.</span><span class="sxs-lookup"><span data-stu-id="5a566-105">The **image** attribute specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="5a566-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5a566-106">Possible Values</span></span>

<span data-ttu-id="5a566-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5a566-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a566-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a566-108">Remarks</span></span>

<span data-ttu-id="5a566-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="5a566-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="5a566-110">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .</span><span class="sxs-lookup"><span data-stu-id="5a566-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="5a566-111">Se a imagem do controle for maior que a região definida, a imagem será cortada.</span><span class="sxs-lookup"><span data-stu-id="5a566-111">If the image of the control is larger than the defined region, the image will be cropped.</span></span>

<span data-ttu-id="5a566-112">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="5a566-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a566-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a566-113">Requirements</span></span>



| <span data-ttu-id="5a566-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a566-114">Requirement</span></span> | <span data-ttu-id="5a566-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5a566-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5a566-116">Versão</span><span class="sxs-lookup"><span data-stu-id="5a566-116">Version</span></span><br/> | <span data-ttu-id="5a566-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5a566-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a566-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a566-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a566-119">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="5a566-119">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="5a566-120">**BUTTON. hueShift**</span><span class="sxs-lookup"><span data-stu-id="5a566-120">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="5a566-121">**BOTÃO. saturação**</span><span class="sxs-lookup"><span data-stu-id="5a566-121">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





