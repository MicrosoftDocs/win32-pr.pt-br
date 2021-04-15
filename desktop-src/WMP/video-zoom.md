---
title: VIDEO. zoom
description: O atributo zoom especifica a porcentagem por meio da qual dimensionar o vídeo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. zoom do Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761067"
---
# <a name="videozoom"></a><span data-ttu-id="95d5c-104">VIDEO. zoom</span><span class="sxs-lookup"><span data-stu-id="95d5c-104">VIDEO.zoom</span></span>

<span data-ttu-id="95d5c-105">O atributo **zoom** especifica a porcentagem por meio da qual dimensionar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="95d5c-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="95d5c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="95d5c-106">Possible Values</span></span>

<span data-ttu-id="95d5c-107">Esse atributo é um **número** de leitura/gravação (**longo**) que varia de 1 até o tamanho máximo acomodado pela largura e altura do controle de vídeo.</span><span class="sxs-lookup"><span data-stu-id="95d5c-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="95d5c-108">Ele tem um valor padrão de 100.</span><span class="sxs-lookup"><span data-stu-id="95d5c-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d5c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="95d5c-109">Remarks</span></span>

<span data-ttu-id="95d5c-110">Esse atributo não pode ser usado em conjunto com o atributo **fullscreen** .</span><span class="sxs-lookup"><span data-stu-id="95d5c-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="95d5c-111">Se a **largura** e a **altura** forem especificadas e a janela de vídeo resultante for maior do que o vídeo que está sendo reproduzido, o vídeo poderá ser ampliado ao escalar verticalmente até o tamanho máximo acomodado pela janela.</span><span class="sxs-lookup"><span data-stu-id="95d5c-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="95d5c-112">Se a **largura** e a **altura** não forem especificadas, o **zoom** será limitado aos valores de 100 ou menos.</span><span class="sxs-lookup"><span data-stu-id="95d5c-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="95d5c-113">Se a propriedade **shrinkToFit** for false, o vídeo mudará a proporção no zoom, para se ajustar ao espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="95d5c-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="95d5c-114">Se **shrinkToFit** for true, o vídeo será reduzido para se ajustar na dimensão mais restritiva, mantendo suas proporções originais.</span><span class="sxs-lookup"><span data-stu-id="95d5c-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d5c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d5c-115">Requirements</span></span>



| <span data-ttu-id="95d5c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d5c-116">Requirement</span></span> | <span data-ttu-id="95d5c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="95d5c-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="95d5c-118">Versão</span><span class="sxs-lookup"><span data-stu-id="95d5c-118">Version</span></span><br/> | <span data-ttu-id="95d5c-119">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="95d5c-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95d5c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="95d5c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d5c-121">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="95d5c-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="95d5c-122">**VÍDEO. tela inteira**</span><span class="sxs-lookup"><span data-stu-id="95d5c-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="95d5c-123">**VÍDEO. shrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="95d5c-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





