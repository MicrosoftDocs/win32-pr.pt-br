---
title: CUSTOMSLIDER.downImage
description: O atributo downImage especifica ou recupera a imagem de estado inferior do controle deslizante personalizado.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794494"
---
# <a name="customsliderdownimage"></a><span data-ttu-id="b0769-104">CUSTOMSLIDER.downImage</span><span class="sxs-lookup"><span data-stu-id="b0769-104">CUSTOMSLIDER.downImage</span></span>

<span data-ttu-id="b0769-105">O atributo **downImage** especifica ou recupera a imagem de estado inferior do controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="b0769-105">The **downImage** attribute specifies or retrieves the down state image of the custom slider.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="b0769-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b0769-106">Possible Values</span></span>

<span data-ttu-id="b0769-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b0769-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0769-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0769-108">Remarks</span></span>

<span data-ttu-id="b0769-109">Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="b0769-109">This attribute is optional.</span></span> <span data-ttu-id="b0769-110">Se não for especificado, o arquivo especificado no atributo **Image** será usado.</span><span class="sxs-lookup"><span data-stu-id="b0769-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="b0769-111">O **downImage** representa o estado inoperante do controle **CUSTOMSLIDER** .</span><span class="sxs-lookup"><span data-stu-id="b0769-111">The **downImage** represents the down state of the **CUSTOMSLIDER** control.</span></span> <span data-ttu-id="b0769-112">Pode ser uma única imagem ou uma série de imagens que representam os vários Estados do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="b0769-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="b0769-113">Se várias imagens forem usadas, elas serão organizadas da mesma maneira que o arquivo de **imagem** .</span><span class="sxs-lookup"><span data-stu-id="b0769-113">If multiple images are used, they are arranged in the same way as the **image** file.</span></span>

<span data-ttu-id="b0769-114">Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).</span><span class="sxs-lookup"><span data-stu-id="b0769-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0769-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0769-115">Requirements</span></span>



| <span data-ttu-id="b0769-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0769-116">Requirement</span></span> | <span data-ttu-id="b0769-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b0769-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b0769-118">Versão</span><span class="sxs-lookup"><span data-stu-id="b0769-118">Version</span></span><br/> | <span data-ttu-id="b0769-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b0769-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0769-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0769-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0769-121">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="b0769-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="b0769-122">**CUSTOMSLIDER. Image**</span><span class="sxs-lookup"><span data-stu-id="b0769-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





