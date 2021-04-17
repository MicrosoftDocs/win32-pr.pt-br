---
title: Exibir. backgroundImage
description: O atributo backgroundImage especifica ou recupera a imagem de plano de fundo da exibição ou da subexibição.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- EXIBIR o Windows Media Player. backgroundImage
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751581"
---
# <a name="viewbackgroundimage"></a><span data-ttu-id="31cc3-104">Exibir. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="31cc3-104">VIEW.backgroundImage</span></span>

<span data-ttu-id="31cc3-105">O atributo **backgroundImage** especifica ou recupera a imagem de plano de fundo da **exibição** ou da **subexibição**.</span><span class="sxs-lookup"><span data-stu-id="31cc3-105">The **backgroundImage** attribute specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="31cc3-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="31cc3-106">Possible Values</span></span>

<span data-ttu-id="31cc3-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="31cc3-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="31cc3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="31cc3-108">Remarks</span></span>

<span data-ttu-id="31cc3-109">Os formatos com suporte são BMP, JPG, GIF e PNG.</span><span class="sxs-lookup"><span data-stu-id="31cc3-109">The supported formats are BMP, JPG, GIF, and PNG.</span></span> <span data-ttu-id="31cc3-110">Se a imagem for um arquivo BMP de 8 bits, seus valores de matiz e de saturação poderão ser alterados dinamicamente usando os atributos **backgroundImageHueShift** e **backgroundImageSaturation** .</span><span class="sxs-lookup"><span data-stu-id="31cc3-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **backgroundImageHueShift** and **backgroundImageSaturation** attributes.</span></span>

<span data-ttu-id="31cc3-111">Em um pacote de download do Windows Media, se você especificar o atributo **backgroundImage** para um elemento **View** , também deverá especificar o atributo **backgroundColor** para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="31cc3-111">In a Windows Media Download package, if you specify the **backgroundImage** attribute for a **VIEW** element, then you must also specify the **backgroundColor** attribute for that element.</span></span>

## <a name="requirements"></a><span data-ttu-id="31cc3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31cc3-112">Requirements</span></span>



| <span data-ttu-id="31cc3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="31cc3-113">Requirement</span></span> | <span data-ttu-id="31cc3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="31cc3-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="31cc3-115">Versão</span><span class="sxs-lookup"><span data-stu-id="31cc3-115">Version</span></span><br/> | <span data-ttu-id="31cc3-116">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="31cc3-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31cc3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="31cc3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cc3-118">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="31cc3-118">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="31cc3-119">**Exibir. backgroundImageHueShift**</span><span class="sxs-lookup"><span data-stu-id="31cc3-119">**VIEW.backgroundImageHueShift**</span></span>](view-backgroundimagehueshift.md)
</dt> <dt>

[<span data-ttu-id="31cc3-120">**Exibir. backgroundImageSaturation**</span><span class="sxs-lookup"><span data-stu-id="31cc3-120">**VIEW.backgroundImageSaturation**</span></span>](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





