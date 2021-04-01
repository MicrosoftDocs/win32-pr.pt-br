---
description: Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado. Esse atributo se aplica a exemplos de mídia.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Atributo MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091056"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="c3cdc-104">\_Atributo MFSampleExtension RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="c3cdc-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="c3cdc-105">Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="c3cdc-106">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3cdc-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c3cdc-107">Data type</span></span>

<span data-ttu-id="c3cdc-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c3cdc-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="c3cdc-109">Get/set</span></span>

<span data-ttu-id="c3cdc-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c3cdc-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c3cdc-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c3cdc-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3cdc-112">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c3cdc-112">Applies to</span></span>

[<span data-ttu-id="c3cdc-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="c3cdc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3cdc-114">Remarks</span></span>

<span data-ttu-id="c3cdc-115">Se o valor for **false** ou o atributo não estiver definido, o primeiro campo não será repetido.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="c3cdc-116">Se o valor for **true**, o primeiro campo será repetido.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="c3cdc-117">O valor **true** é válido somente quando as seguintes condições são verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="c3cdc-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="c3cdc-118">O tipo de mídia é entrelaçado misto e progressivo.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="c3cdc-119">(O atributo de atributo do [**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md) no tipo de mídia é **MFVideoInterlace \_ MixedInterlaceOrProgressive**.)</span><span class="sxs-lookup"><span data-stu-id="c3cdc-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="c3cdc-120">O quadro é progressivo e o atributo [**\_ entrelaçado MFSampleExtension**](mfsampleextension-interlaced-attribute.md) no exemplo é **true**.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="c3cdc-121">O atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) é definido no exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="c3cdc-122">O valor pode ser **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="c3cdc-123">A ordenação dos campos é determinada por esse atributo.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="c3cdc-124">Esse atributo é usado para a busca de 3:2.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="c3cdc-125">A tabela a seguir mostra a ordem na qual os campos são exibidos.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="c3cdc-126">MFSampleExtension \_ RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="c3cdc-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="c3cdc-127">MFSampleExtension \_ BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="c3cdc-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="c3cdc-128">Ordem dos campos</span><span class="sxs-lookup"><span data-stu-id="c3cdc-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="c3cdc-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-129">**TRUE**</span></span>                            | <span data-ttu-id="c3cdc-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-130">**TRUE**</span></span>                            | <span data-ttu-id="c3cdc-131">Inferior, superior, inferior</span><span class="sxs-lookup"><span data-stu-id="c3cdc-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="c3cdc-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-132">**TRUE**</span></span>                            | <span data-ttu-id="c3cdc-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-133">**FALSE**</span></span>                           | <span data-ttu-id="c3cdc-134">Superior, inferior, superior</span><span class="sxs-lookup"><span data-stu-id="c3cdc-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="c3cdc-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-135">**FALSE**</span></span>                           | <span data-ttu-id="c3cdc-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-136">**TRUE**</span></span>                            | <span data-ttu-id="c3cdc-137">Inferior, superior</span><span class="sxs-lookup"><span data-stu-id="c3cdc-137">Lower, upper</span></span>        |
| <span data-ttu-id="c3cdc-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-138">**FALSE**</span></span>                           | <span data-ttu-id="c3cdc-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="c3cdc-139">**FALSE**</span></span>                           | <span data-ttu-id="c3cdc-140">Superior, inferior</span><span class="sxs-lookup"><span data-stu-id="c3cdc-140">Upper, lower</span></span>        |



 

<span data-ttu-id="c3cdc-141">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c3cdc-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cdc-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3cdc-142">Requirements</span></span>



| <span data-ttu-id="c3cdc-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3cdc-143">Requirement</span></span> | <span data-ttu-id="c3cdc-144">Valor</span><span class="sxs-lookup"><span data-stu-id="c3cdc-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cdc-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3cdc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cdc-146">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3cdc-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c3cdc-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3cdc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cdc-148">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c3cdc-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c3cdc-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3cdc-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3cdc-150"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cdc-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cdc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3cdc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cdc-152">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c3cdc-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3cdc-153">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="c3cdc-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3cdc-154">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="c3cdc-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="c3cdc-155">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="c3cdc-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




