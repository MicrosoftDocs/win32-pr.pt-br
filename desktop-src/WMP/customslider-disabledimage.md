---
title: CUSTOMSLIDER.disabledImage
description: O atributo disabledImage especifica ou recupera a imagem do controle deslizante usado quando o controle deslizante está desabilitado.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813175"
---
# <a name="customsliderdisabledimage"></a><span data-ttu-id="d0ca5-104">CUSTOMSLIDER.disabledImage</span><span class="sxs-lookup"><span data-stu-id="d0ca5-104">CUSTOMSLIDER.disabledImage</span></span>

<span data-ttu-id="d0ca5-105">O atributo **disabledImage** especifica ou recupera a imagem do controle deslizante usado quando o controle deslizante está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d0ca5-105">The **disabledImage** attribute specifies or retrieves the image of the slider used when the slider is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="d0ca5-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d0ca5-106">Possible Values</span></span>

<span data-ttu-id="d0ca5-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="d0ca5-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ca5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0ca5-108">Remarks</span></span>

<span data-ttu-id="d0ca5-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="d0ca5-109">This attribute is optional.</span></span> <span data-ttu-id="d0ca5-110">Se não for especificado, o arquivo especificado no atributo **Image** será usado.</span><span class="sxs-lookup"><span data-stu-id="d0ca5-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="d0ca5-111">O **disabledImage** representa o estado desabilitado do controle **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="d0ca5-111">The **disabledImage** represents the disabled state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="d0ca5-112">Pode ser uma única imagem ou uma série de imagens que representam os vários Estados do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="d0ca5-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="d0ca5-113">Se várias imagens forem usadas, elas serão organizadas da mesma maneira que o arquivo de **imagem** .</span><span class="sxs-lookup"><span data-stu-id="d0ca5-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="d0ca5-114">Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="d0ca5-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ca5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0ca5-115">Requirements</span></span>



| <span data-ttu-id="d0ca5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ca5-116">Requirement</span></span> | <span data-ttu-id="d0ca5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d0ca5-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d0ca5-118">Versão</span><span class="sxs-lookup"><span data-stu-id="d0ca5-118">Version</span></span><br/> | <span data-ttu-id="d0ca5-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d0ca5-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0ca5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0ca5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ca5-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="d0ca5-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="d0ca5-122">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="d0ca5-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





