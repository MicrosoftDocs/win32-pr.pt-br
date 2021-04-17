---
description: O \_ tipo de enumeração de tipos de verificação de vídeo WPD \_ \_ descreve como os campos em um arquivo de vídeo são codificados.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumeração de WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749701"
---
# <a name="wpd_video_scan_types-enumeration"></a><span data-ttu-id="4fab1-103">\_Enumeração de \_ tipos de verificação de vídeo WPD \_</span><span class="sxs-lookup"><span data-stu-id="4fab1-103">WPD\_VIDEO\_SCAN\_TYPES enumeration</span></span>

<span data-ttu-id="4fab1-104">O tipo de enumeração de **\_ tipos de \_ verificação \_ de vídeo WPD** descreve como os campos em um arquivo de vídeo são codificados.</span><span class="sxs-lookup"><span data-stu-id="4fab1-104">The **WPD\_VIDEO\_SCAN\_TYPES** enumeration type describes how the fields in a video file are encoded.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fab1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fab1-105">Syntax</span></span>


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="4fab1-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="4fab1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="4fab1-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_tipo de exame de vídeo WPD \_ \_ \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="4fab1-107"><span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**WPD\_VIDEO\_SCAN\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-108">O tipo de verificação não foi definido para este arquivo de vídeo ou não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="4fab1-108">The scan type has not been defined for this video file, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_tipo de exame de vídeo WPD \_ \_ \_ progressivo**</span><span class="sxs-lookup"><span data-stu-id="4fab1-109"><span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-110">Um arquivo de vídeo de verificação progressiva.</span><span class="sxs-lookup"><span data-stu-id="4fab1-110">A progressive scan video file.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**\_campo de tipo de verificação de vídeo WPD \_ \_ \_ \_ intercalado \_ superior \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="4fab1-111"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-112">Um arquivo de vídeo intercalado no qual os campos são alternativos e o campo superior (com linha 1) é desenhado primeiro.</span><span class="sxs-lookup"><span data-stu-id="4fab1-112">An interleaved video file where the fields alternate and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="4fab1-113">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="4fab1-113">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_campo de tipo de verificação de vídeo WPD \_ \_ \_ \_ intercalado \_ mais baixo \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="4fab1-114"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-115">Um arquivo de vídeo intercalado no qual os campos são alternativos e o campo inferior (com linha 2) é desenhado primeiro.</span><span class="sxs-lookup"><span data-stu-id="4fab1-115">An interleaved video file where the fields alternate and the lower field (with line 2) is drawn first.</span></span> <span data-ttu-id="4fab1-116">Para obter mais informações, consulte comentários, seguindo esta seção.</span><span class="sxs-lookup"><span data-stu-id="4fab1-116">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**campo de tipo de verificação de vídeo WPD- \_ \_ \_ \_ \_ único \_ superior \_ primeiro**</span><span class="sxs-lookup"><span data-stu-id="4fab1-117"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_UPPER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-118">Um arquivo de vídeo intercalado em que os campos são enviados como amostras contíguas e o campo superior (com a linha 1) é desenhado primeiro.</span><span class="sxs-lookup"><span data-stu-id="4fab1-118">An interleaved video file where the fields are sent as contiguous samples and the upper field (with line 1) is drawn first.</span></span> <span data-ttu-id="4fab1-119">Para obter mais informações, consulte comentários, seguindo esta seção.</span><span class="sxs-lookup"><span data-stu-id="4fab1-119">For more information, see Remarks, following this section.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**campo de tipo de verificação de vídeo WPD- \_ \_ \_ \_ \_ \_ \_ primeiro inferior**</span><span class="sxs-lookup"><span data-stu-id="4fab1-120"><span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE\_LOWER\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-121">Um arquivo de vídeo intercalado em que os campos são enviados como amostras contíguas e o campo inferior (com linha 2) é enviado primeiro.</span><span class="sxs-lookup"><span data-stu-id="4fab1-121">An interleaved video file where the fields are sent as contiguous samples and the lower field (with line 2) is sent first.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_exame de vídeo WPD \_ \_ tipo \_ \_ entrelaçado misto**</span><span class="sxs-lookup"><span data-stu-id="4fab1-122"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-123">Um arquivo de vídeo com uma combinação de modos de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="4fab1-123">A video file with a mix of interlacing modes.</span></span>

</dd> <dt>

<span data-ttu-id="4fab1-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ exame de vídeo \_ WPD \_ tipo \_ entrelaçado misto \_ e \_ progressivo**</span><span class="sxs-lookup"><span data-stu-id="4fab1-124"><span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD\_VIDEO\_SCAN\_TYPE\_MIXED\_INTERLACE\_AND\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="4fab1-125">Um arquivo de vídeo com uma combinação de modos entrelaçados e progressivos.</span><span class="sxs-lookup"><span data-stu-id="4fab1-125">A video file with a mix of interlaced and progressive modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fab1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fab1-126">Remarks</span></span>

<span data-ttu-id="4fab1-127">Essa enumeração é usada pela propriedade [de \_ \_ \_ tipo de verificação de vídeo WPD](properties-and-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4fab1-127">This enumeration is used by the [WPD\_VIDEO\_SCAN\_TYPE](properties-and-attributes.md) property.</span></span>

<span data-ttu-id="4fab1-128">Há dois tipos de formatos de arquivo intercalados que são especificados por essa enumeração.</span><span class="sxs-lookup"><span data-stu-id="4fab1-128">There are two types of interleaved file formats that are specified by this enumeration.</span></span> <span data-ttu-id="4fab1-129">**WPD \_ O \_ campo de tipo de verificação de vídeo \_ \_ \_ intercalado** refere-se a um formato de arquivo em que os quadros são entregues, pois eles eram campos digitalizados e os dados são colocados em linha por linha, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="4fab1-129">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_INTERLEAVED** refers to a file format where frames are delivered as they were scanned fields alternate and data goes line by line, as shown here:</span></span>

<span data-ttu-id="4fab1-130">**Quadro 1**</span><span class="sxs-lookup"><span data-stu-id="4fab1-130">**Frame 1**</span></span>

<span data-ttu-id="4fab1-131">Campo 1: linha 1</span><span class="sxs-lookup"><span data-stu-id="4fab1-131">Field 1: Line 1</span></span>

<span data-ttu-id="4fab1-132">Campo 2: linha 1</span><span class="sxs-lookup"><span data-stu-id="4fab1-132">Field 2: Line 1</span></span>

<span data-ttu-id="4fab1-133">Campo 1: linha 2</span><span class="sxs-lookup"><span data-stu-id="4fab1-133">Field 1: Line 2</span></span>

<span data-ttu-id="4fab1-134">Campo 2: linha 2</span><span class="sxs-lookup"><span data-stu-id="4fab1-134">Field 2: Line 2</span></span>

<span data-ttu-id="4fab1-135">Campo 1: linha 3</span><span class="sxs-lookup"><span data-stu-id="4fab1-135">Field 1: Line 3</span></span>

<span data-ttu-id="4fab1-136">Campo 2: linha 3</span><span class="sxs-lookup"><span data-stu-id="4fab1-136">Field 2: Line 3</span></span>

<span data-ttu-id="4fab1-137">...</span><span class="sxs-lookup"><span data-stu-id="4fab1-137">...</span></span>

<span data-ttu-id="4fab1-138">**WPD \_ Campo de tipo de verificação de vídeo \_ \_ \_ \_ único** refere-se a um formato de arquivo em que cada campo é armazenado em um único bloco de linhas de varredura, e os campos são armazenados em sequência, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="4fab1-138">**WPD\_VIDEO\_SCAN\_TYPE\_FIELD\_SINGLE** refers to a file format where each field is stored in a single block of scan lines, and fields are stored sequentially, as shown here:</span></span>

<span data-ttu-id="4fab1-139">**Quadro 1**</span><span class="sxs-lookup"><span data-stu-id="4fab1-139">**Frame 1**</span></span>

<span data-ttu-id="4fab1-140">Campo 1: linha 1</span><span class="sxs-lookup"><span data-stu-id="4fab1-140">Field 1: Line 1</span></span>

<span data-ttu-id="4fab1-141">Campo 1: linha 2</span><span class="sxs-lookup"><span data-stu-id="4fab1-141">Field 1: Line 2</span></span>

<span data-ttu-id="4fab1-142">Campo 1: linha 3</span><span class="sxs-lookup"><span data-stu-id="4fab1-142">Field 1: Line 3</span></span>

<span data-ttu-id="4fab1-143">...</span><span class="sxs-lookup"><span data-stu-id="4fab1-143">...</span></span>

<span data-ttu-id="4fab1-144">Seguido por</span><span class="sxs-lookup"><span data-stu-id="4fab1-144">Followed by</span></span>

<span data-ttu-id="4fab1-145">Campo 2: linha 1</span><span class="sxs-lookup"><span data-stu-id="4fab1-145">Field 2: Line 1</span></span>

<span data-ttu-id="4fab1-146">Campo 2: linha 2</span><span class="sxs-lookup"><span data-stu-id="4fab1-146">Field 2: Line 2</span></span>

<span data-ttu-id="4fab1-147">Campo 2: linha 3</span><span class="sxs-lookup"><span data-stu-id="4fab1-147">Field 2: Line 3</span></span>

<span data-ttu-id="4fab1-148">...</span><span class="sxs-lookup"><span data-stu-id="4fab1-148">...</span></span>

## <a name="requirements"></a><span data-ttu-id="4fab1-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fab1-149">Requirements</span></span>



| <span data-ttu-id="4fab1-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fab1-150">Requirement</span></span> | <span data-ttu-id="4fab1-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4fab1-151">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fab1-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4fab1-152">Header</span></span><br/> | <dl> <span data-ttu-id="4fab1-153"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fab1-153"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fab1-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fab1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fab1-155">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="4fab1-155">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




