---
title: BUTTON. downImage
description: O atributo downImage especifica ou recupera o nome da imagem que representa o estado inoperante do botão.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- DownImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781270"
---
# <a name="buttongroupdownimage"></a><span data-ttu-id="24c84-104">BUTTON. downImage</span><span class="sxs-lookup"><span data-stu-id="24c84-104">BUTTONGROUP.downImage</span></span>

<span data-ttu-id="24c84-105">O atributo **downImage** especifica ou recupera o nome da imagem que representa o estado inoperante do **botão**.</span><span class="sxs-lookup"><span data-stu-id="24c84-105">The **downImage** attribute specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="24c84-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="24c84-106">Possible Values</span></span>

<span data-ttu-id="24c84-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="24c84-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24c84-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="24c84-108">Remarks</span></span>

<span data-ttu-id="24c84-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="24c84-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="24c84-110">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .</span><span class="sxs-lookup"><span data-stu-id="24c84-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="24c84-111">A imagem padrão é aquela especificada no atributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="24c84-111">The default image is the one specified in the **image** attribute.</span></span>

<span data-ttu-id="24c84-112">Se a imagem inoperante for maior que a região definida, a imagem abaixo será cortada.</span><span class="sxs-lookup"><span data-stu-id="24c84-112">If the down image is larger than the defined region, the down image will be cropped.</span></span>

<span data-ttu-id="24c84-113">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="24c84-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="24c84-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24c84-114">Requirements</span></span>



| <span data-ttu-id="24c84-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24c84-115">Requirement</span></span> | <span data-ttu-id="24c84-116">Valor</span><span class="sxs-lookup"><span data-stu-id="24c84-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="24c84-117">Versão</span><span class="sxs-lookup"><span data-stu-id="24c84-117">Version</span></span><br/> | <span data-ttu-id="24c84-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="24c84-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24c84-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="24c84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24c84-120">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="24c84-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="24c84-121">**BUTTON. hueShift**</span><span class="sxs-lookup"><span data-stu-id="24c84-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="24c84-122">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="24c84-122">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="24c84-123">**BOTÃO. saturação**</span><span class="sxs-lookup"><span data-stu-id="24c84-123">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





