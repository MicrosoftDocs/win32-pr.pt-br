---
description: Esses sinalizadores especificam como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Redimensionar sinalizadores (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758831"
---
# <a name="resize-flags"></a><span data-ttu-id="f693f-103">Redimensionar sinalizadores</span><span class="sxs-lookup"><span data-stu-id="f693f-103">Resize Flags</span></span>

<span data-ttu-id="f693f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f693f-104">\[Deprecated.</span></span> <span data-ttu-id="f693f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f693f-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="f693f-106">Esses sinalizadores especificam como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.</span><span class="sxs-lookup"><span data-stu-id="f693f-106">These flags specify how a video source is rendered if its size does not match the output dimensions.</span></span>



| <span data-ttu-id="f693f-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f693f-107">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="f693f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f693f-108">Description</span></span>                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <span data-ttu-id="f693f-109"><dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f693f-109"><dt>**RESIZEF\_STRETCH**</dt> <dt>0</dt></span></span> </dl>                                                                          | <span data-ttu-id="f693f-110">A imagem é ampliada para se ajustar ao tamanho do quadro de destino em ambas as dimensões, sem preservar a taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="f693f-110">The image is stretched to fit the target frame size in both dimensions, without preserving the aspect ratio.</span></span><br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <span data-ttu-id="f693f-111"><dt>**RESIZEF \_ CORTAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f693f-111"><dt>**RESIZEF\_CROP**</dt> <dt>1</dt></span></span> </dl>                                                                                   | <span data-ttu-id="f693f-112">A imagem não foi redimensionada.</span><span class="sxs-lookup"><span data-stu-id="f693f-112">The image is not resized.</span></span> <span data-ttu-id="f693f-113">Se a imagem for menor do que o quadro de destino, a área ao redor será preta.</span><span class="sxs-lookup"><span data-stu-id="f693f-113">If the image is smaller than the target frame, the surrounding area is black.</span></span> <span data-ttu-id="f693f-114">Se a imagem for maior que o quadro de destino, a imagem será cortada.</span><span class="sxs-lookup"><span data-stu-id="f693f-114">If the image is larger than the target frame, the image is cropped.</span></span><br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <span data-ttu-id="f693f-115"><dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f693f-115"><dt>**RESIZEF\_PRESERVEASPECTRATIO**</dt> <dt>2</dt></span></span> </dl>                                      | <span data-ttu-id="f693f-116">A imagem é redimensionada para se ajustar ao quadro de destino ao longo de uma dimensão, preservando a taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="f693f-116">The image is resized to fit the target frame along one dimension, while preserving the aspect ratio.</span></span> <span data-ttu-id="f693f-117">Se a taxa de largura para altura na imagem não corresponder à taxa no quadro de destino, ela criará um letterbox.</span><span class="sxs-lookup"><span data-stu-id="f693f-117">If the ratio of width to height in the image does not match the ratio in the target frame, it creates a letterbox.</span></span><br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <span data-ttu-id="f693f-118"><dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f693f-118"><dt>**RESIZEF\_PRESERVEASPECTRATIO\_NOLETTERBOX**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="f693f-119">A imagem é redimensionada para preencher o quadro de destino inteiro, preservando a taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="f693f-119">The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span> <span data-ttu-id="f693f-120">Em vez de criar um Letterbox, esse modo corta a imagem, seja ao longo dos lados ou entre as partes superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="f693f-120">Rather than create a letterbox, this mode crops the image, either along the sides or across the top and bottom.</span></span><br/>                 |



## <a name="remarks"></a><span data-ttu-id="f693f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f693f-121">Remarks</span></span>

<span data-ttu-id="f693f-122">As imagens a seguir mostram os efeitos desses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="f693f-122">The following images show the effects of these flags.</span></span>

![redimensionar sinalizadores](images/stretch14.png)

## <a name="requirements"></a><span data-ttu-id="f693f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f693f-124">Requirements</span></span>



| <span data-ttu-id="f693f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f693f-125">Requirement</span></span> | <span data-ttu-id="f693f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f693f-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f693f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f693f-127">Header</span></span><br/> | <dl> <span data-ttu-id="f693f-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f693f-128"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f693f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f693f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f693f-130">**IAMTimelineSrc:: getstretchmode**</span><span class="sxs-lookup"><span data-stu-id="f693f-130">**IAMTimelineSrc::GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[<span data-ttu-id="f693f-131">**IAMTimelineSrc:: setalongamode**</span><span class="sxs-lookup"><span data-stu-id="f693f-131">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




