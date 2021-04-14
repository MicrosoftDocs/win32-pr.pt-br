---
description: Para um formato de vídeo 3D, especifica qual exibição é a exibição à esquerda.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Atributo MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370785"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a><span data-ttu-id="cfcef-103">O \_ \_ atributo 3D de vídeo MF MT \_ \_ First \_ é \_ Left</span><span class="sxs-lookup"><span data-stu-id="cfcef-103">MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute</span></span>

<span data-ttu-id="cfcef-104">Para um formato de vídeo 3D, especifica qual exibição é a exibição à esquerda.</span><span class="sxs-lookup"><span data-stu-id="cfcef-104">For a 3D video format, specifies which view is the left view.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfcef-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cfcef-105">Data type</span></span>

<span data-ttu-id="cfcef-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="cfcef-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcef-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfcef-107">Remarks</span></span>

<span data-ttu-id="cfcef-108">Para vídeo 3D, cada amostra de vídeo contém duas exibições, que são designadas *primeira exibição* e *segunda exibição*.</span><span class="sxs-lookup"><span data-stu-id="cfcef-108">For 3D video, each video sample contains two views, which are designated *first view* and *second view*.</span></span> <span data-ttu-id="cfcef-109">O layout exato das exibições na memória é indicado pelo atributo [de \_ \_ \_ \_ formato 3D de vídeo MF MT](mf-mt-video-3d-format.md) .</span><span class="sxs-lookup"><span data-stu-id="cfcef-109">The exact layout of the views in memory is indicated by the [MF\_MT\_VIDEO\_3D\_FORMAT](mf-mt-video-3d-format.md) attribute.</span></span>



| <span data-ttu-id="cfcef-110">Formatar</span><span class="sxs-lookup"><span data-stu-id="cfcef-110">Format</span></span>               | <span data-ttu-id="cfcef-111">Primeira exibição</span><span class="sxs-lookup"><span data-stu-id="cfcef-111">First View</span></span>              | <span data-ttu-id="cfcef-112">Segunda exibição</span><span class="sxs-lookup"><span data-stu-id="cfcef-112">Second View</span></span>               |
|----------------------|-------------------------|---------------------------|
| <span data-ttu-id="cfcef-113">Empacotado lado a lado</span><span class="sxs-lookup"><span data-stu-id="cfcef-113">Packed side-by-side</span></span>  | <span data-ttu-id="cfcef-114">Metade esquerda do buffer</span><span class="sxs-lookup"><span data-stu-id="cfcef-114">Left half of the buffer</span></span> | <span data-ttu-id="cfcef-115">Metade direita do buffer</span><span class="sxs-lookup"><span data-stu-id="cfcef-115">Right half of the buffer</span></span>  |
| <span data-ttu-id="cfcef-116">De cima para baixo embalado</span><span class="sxs-lookup"><span data-stu-id="cfcef-116">Packed top-to-bottom</span></span> | <span data-ttu-id="cfcef-117">Metade superior do buffer</span><span class="sxs-lookup"><span data-stu-id="cfcef-117">Top half of the buffer</span></span>  | <span data-ttu-id="cfcef-118">Metade inferior do buffer</span><span class="sxs-lookup"><span data-stu-id="cfcef-118">Bottom half of the buffer</span></span> |
| <span data-ttu-id="cfcef-119">Visões</span><span class="sxs-lookup"><span data-stu-id="cfcef-119">Multiview</span></span>            | <span data-ttu-id="cfcef-120">Índice de buffer 0</span><span class="sxs-lookup"><span data-stu-id="cfcef-120">Buffer index 0</span></span>          | <span data-ttu-id="cfcef-121">Índice de buffer 1</span><span class="sxs-lookup"><span data-stu-id="cfcef-121">Buffer index 1</span></span>            |
| <span data-ttu-id="cfcef-122">Exibição de base</span><span class="sxs-lookup"><span data-stu-id="cfcef-122">Base view</span></span>            | <span data-ttu-id="cfcef-123">Quadro inteiro</span><span class="sxs-lookup"><span data-stu-id="cfcef-123">Entire frame</span></span>            | <span data-ttu-id="cfcef-124">Não está presente</span><span class="sxs-lookup"><span data-stu-id="cfcef-124">Not present</span></span>               |



 

<span data-ttu-id="cfcef-125">Por padrão, a primeira exibição é a exibição à esquerda e a segunda exibição é a exibição correta.</span><span class="sxs-lookup"><span data-stu-id="cfcef-125">By default, the first view is the left view, and the second view is the right view.</span></span> <span data-ttu-id="cfcef-126">Se os modos de exibição esquerdo e direito forem trocados, defina \_ o \_ atributo MF MT Video \_ 3D \_ primeiro \_ is \_ Left como **false** no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cfcef-126">If the left and right views are swapped, set the MF\_MT\_VIDEO\_3D\_FIRST\_IS\_LEFT attribute to **FALSE** in the media type.</span></span>

> [!Note]  
> <span data-ttu-id="cfcef-127">No formato de *exibição de base* (**MFVideo3DSampleFormat \_ BaseView**), somente a exibição de base é mantida, portanto, esse atributo não se aplica.</span><span class="sxs-lookup"><span data-stu-id="cfcef-127">In *base view* format (**MFVideo3DSampleFormat\_BaseView**), only the base view is retained, so this attribute does not apply.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfcef-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfcef-128">Requirements</span></span>



| <span data-ttu-id="cfcef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfcef-129">Requirement</span></span> | <span data-ttu-id="cfcef-130">Valor</span><span class="sxs-lookup"><span data-stu-id="cfcef-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcef-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfcef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cfcef-132">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfcef-132">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cfcef-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfcef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cfcef-134">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfcef-134">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cfcef-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfcef-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfcef-136"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfcef-136"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcef-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfcef-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcef-138">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfcef-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




