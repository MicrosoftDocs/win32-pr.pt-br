---
title: BUTTON. downImage
description: O atributo downImage especifica ou recupera a imagem que representa o estado inoperante do botão.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759736"
---
# <a name="buttondownimage"></a><span data-ttu-id="98229-104">BUTTON. downImage</span><span class="sxs-lookup"><span data-stu-id="98229-104">BUTTON.downImage</span></span>

<span data-ttu-id="98229-105">O atributo **downImage** especifica ou recupera a imagem que representa o estado inoperante do **botão**.</span><span class="sxs-lookup"><span data-stu-id="98229-105">The **downImage** attribute specifies or retrieves the image representing the down state of the **BUTTON**.</span></span>

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a><span data-ttu-id="98229-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="98229-106">Possible Values</span></span>

<span data-ttu-id="98229-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome do arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="98229-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="98229-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="98229-108">Remarks</span></span>

<span data-ttu-id="98229-109">Os formatos de imagem com suporte são BMP, JPG, PNG e GIF.</span><span class="sxs-lookup"><span data-stu-id="98229-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="98229-110">A imagem padrão é aquela especificada no atributo **Image** ou seu padrão.</span><span class="sxs-lookup"><span data-stu-id="98229-110">The default image is the one specified in the **image** attribute, or its default.</span></span>

<span data-ttu-id="98229-111">Se a imagem inoperante for maior do que a região definida no atributo ambiente, a imagem abaixo será cortada.</span><span class="sxs-lookup"><span data-stu-id="98229-111">If the down image is larger than the defined region in the ambient attribute, the down image will be cropped.</span></span>

<span data-ttu-id="98229-112">Se a imagem não puder ser recuperada, uma imagem padrão (a imagem vermelha-x) será exibida.</span><span class="sxs-lookup"><span data-stu-id="98229-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="98229-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98229-113">Requirements</span></span>



| <span data-ttu-id="98229-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98229-114">Requirement</span></span> | <span data-ttu-id="98229-115">Valor</span><span class="sxs-lookup"><span data-stu-id="98229-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="98229-116">Versão</span><span class="sxs-lookup"><span data-stu-id="98229-116">Version</span></span><br/> | <span data-ttu-id="98229-117">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="98229-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98229-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="98229-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98229-119">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="98229-119">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="98229-120">**BOTÃO. para baixo**</span><span class="sxs-lookup"><span data-stu-id="98229-120">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="98229-121">**BOTÃO. imagem**</span><span class="sxs-lookup"><span data-stu-id="98229-121">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





