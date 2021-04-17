---
title: BUTTON. disabledImage
description: O atributo disabledImage especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no botão.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- DisabledImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763368"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="a9212-104">BUTTON. disabledImage</span><span class="sxs-lookup"><span data-stu-id="a9212-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="a9212-105">O atributo **disabledImage** especifica ou recupera o nome da imagem que representa o estado desabilitado dos botões no **botão**.</span><span class="sxs-lookup"><span data-stu-id="a9212-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="a9212-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="a9212-106">Possible Values</span></span>

<span data-ttu-id="a9212-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a9212-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9212-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9212-108">Remarks</span></span>

<span data-ttu-id="a9212-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="a9212-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="a9212-110">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **hueShift** e **saturação** .</span><span class="sxs-lookup"><span data-stu-id="a9212-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="a9212-111">Quando o atributo **Disabled** de um elemento **buttonelement** é definido como true, a região correspondente do **DisabledImage** para o grupo de **botões** é exibida.</span><span class="sxs-lookup"><span data-stu-id="a9212-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="a9212-112">Se a imagem desabilitada for maior que a região definida, a imagem desabilitada será cortada.</span><span class="sxs-lookup"><span data-stu-id="a9212-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="a9212-113">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="a9212-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9212-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9212-114">Requirements</span></span>



| <span data-ttu-id="a9212-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9212-115">Requirement</span></span> | <span data-ttu-id="a9212-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a9212-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a9212-117">Versão</span><span class="sxs-lookup"><span data-stu-id="a9212-117">Version</span></span><br/> | <span data-ttu-id="a9212-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a9212-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9212-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9212-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9212-120">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="a9212-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="a9212-121">**BUTTON. hueShift**</span><span class="sxs-lookup"><span data-stu-id="a9212-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="a9212-122">**BOTÃO. saturação**</span><span class="sxs-lookup"><span data-stu-id="a9212-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





