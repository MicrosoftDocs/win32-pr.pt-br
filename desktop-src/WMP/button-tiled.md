---
title: BOTÃO. xadrez
description: O atributo de sublado especifica ou recupera um valor que indica se a imagem do botão será colocada em lado.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BOTÃO. xadrez Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794509"
---
# <a name="buttontiled"></a><span data-ttu-id="639f1-104">BOTÃO. xadrez</span><span class="sxs-lookup"><span data-stu-id="639f1-104">BUTTON.tiled</span></span>

<span data-ttu-id="639f1-105">O atributo de **sublado** especifica ou recupera um valor que indica se a imagem do **botão** será colocada em lado.</span><span class="sxs-lookup"><span data-stu-id="639f1-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="639f1-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="639f1-106">Possible Values</span></span>

<span data-ttu-id="639f1-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="639f1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="639f1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="639f1-108">Value</span></span> | <span data-ttu-id="639f1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="639f1-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="639f1-110">true</span><span class="sxs-lookup"><span data-stu-id="639f1-110">true</span></span>  | <span data-ttu-id="639f1-111">O lado da imagem será enfeita.</span><span class="sxs-lookup"><span data-stu-id="639f1-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="639f1-112">false</span><span class="sxs-lookup"><span data-stu-id="639f1-112">false</span></span> | <span data-ttu-id="639f1-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="639f1-113">Default.</span></span> <span data-ttu-id="639f1-114">A imagem não será enlado.</span><span class="sxs-lookup"><span data-stu-id="639f1-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="639f1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="639f1-115">Remarks</span></span>

<span data-ttu-id="639f1-116">Se a imagem for menor do que a região real do controle, o agrupamento da imagem será repetido até que ela preencha toda a região.</span><span class="sxs-lookup"><span data-stu-id="639f1-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="639f1-117">Se uma imagem não for especificada ou não puder ser recuperada, os **ladrilhos** serão definidos como false.</span><span class="sxs-lookup"><span data-stu-id="639f1-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="639f1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="639f1-118">Requirements</span></span>



| <span data-ttu-id="639f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="639f1-119">Requirement</span></span> | <span data-ttu-id="639f1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="639f1-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="639f1-121">Versão</span><span class="sxs-lookup"><span data-stu-id="639f1-121">Version</span></span><br/> | <span data-ttu-id="639f1-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="639f1-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="639f1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="639f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639f1-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="639f1-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="639f1-125">**BOTÃO. imagem**</span><span class="sxs-lookup"><span data-stu-id="639f1-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





