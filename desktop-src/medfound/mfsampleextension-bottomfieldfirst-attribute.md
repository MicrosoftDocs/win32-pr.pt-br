---
description: Especifica o campo predominância para um quadro de vídeo entrelaçado.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Atributo MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296622"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a><span data-ttu-id="aed21-103">\_Atributo MFSampleExtension BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="aed21-103">MFSampleExtension\_BottomFieldFirst attribute</span></span>

<span data-ttu-id="aed21-104">Especifica o campo predominância para um quadro de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="aed21-104">Specifies the field dominance for an interlaced video frame.</span></span> <span data-ttu-id="aed21-105">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="aed21-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="aed21-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aed21-106">Data type</span></span>

<span data-ttu-id="aed21-107">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="aed21-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="aed21-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="aed21-108">Get/set</span></span>

<span data-ttu-id="aed21-109">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="aed21-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="aed21-110">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="aed21-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="aed21-111">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="aed21-111">Applies to</span></span>

[<span data-ttu-id="aed21-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="aed21-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="aed21-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aed21-113">Remarks</span></span>

<span data-ttu-id="aed21-114">Se o quadro de vídeo estiver entrelaçado e o exemplo contiver dois campos intercalados, esse atributo indicará qual campo será exibido primeiro.</span><span class="sxs-lookup"><span data-stu-id="aed21-114">If the video frame is interlaced and the sample contains two interleaved fields, this attribute indicates which field is displayed first.</span></span> <span data-ttu-id="aed21-115">Se **for true**, o campo inferior será o primeiro a ser atingido.</span><span class="sxs-lookup"><span data-stu-id="aed21-115">If **TRUE**, the bottom field is first in time.</span></span> <span data-ttu-id="aed21-116">Se for **false**, o campo superior será primeiro.</span><span class="sxs-lookup"><span data-stu-id="aed21-116">If **FALSE**, the top field is first.</span></span>

<span data-ttu-id="aed21-117">Se o quadro estiver entrelaçado e o exemplo contiver um único campo, esse atributo indicará qual campo contém o exemplo.</span><span class="sxs-lookup"><span data-stu-id="aed21-117">If the frame is interlaced and the sample contains a single field, this attribute indicates which field the sample contains.</span></span> <span data-ttu-id="aed21-118">Se **for true**, o exemplo conterá o campo inferior.</span><span class="sxs-lookup"><span data-stu-id="aed21-118">If **TRUE**, the sample contains the bottom field.</span></span> <span data-ttu-id="aed21-119">Se **for false**, o exemplo conterá o campo superior.</span><span class="sxs-lookup"><span data-stu-id="aed21-119">If **FALSE**, the sample contains the top field.</span></span>

<span data-ttu-id="aed21-120">Se o quadro for progressivo, esse atributo descreverá como os campos devem ser ordenados quando a saída for entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="aed21-120">If the frame is progressive, this attribute describes how the fields should be ordered when the output is interlaced.</span></span> <span data-ttu-id="aed21-121">Se **for true**, o campo inferior deverá ser de saída primeiro.</span><span class="sxs-lookup"><span data-stu-id="aed21-121">If **TRUE**, the bottom field should be output first.</span></span> <span data-ttu-id="aed21-122">Se **for false**, o campo superior deverá ser de saída primeiro.</span><span class="sxs-lookup"><span data-stu-id="aed21-122">If **FALSE**, the top field should be output first.</span></span>

<span data-ttu-id="aed21-123">Se esse atributo não estiver definido, o tipo de mídia descreverá o campo predominância.</span><span class="sxs-lookup"><span data-stu-id="aed21-123">If this attribute not set, the media type describes the field dominance.</span></span>

<span data-ttu-id="aed21-124">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="aed21-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed21-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aed21-125">Requirements</span></span>



| <span data-ttu-id="aed21-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aed21-126">Requirement</span></span> | <span data-ttu-id="aed21-127">Valor</span><span class="sxs-lookup"><span data-stu-id="aed21-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aed21-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aed21-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aed21-129">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="aed21-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="aed21-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aed21-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aed21-131">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="aed21-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="aed21-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aed21-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="aed21-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aed21-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aed21-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="aed21-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed21-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aed21-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="aed21-136">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="aed21-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="aed21-137">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="aed21-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="aed21-138">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="aed21-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




