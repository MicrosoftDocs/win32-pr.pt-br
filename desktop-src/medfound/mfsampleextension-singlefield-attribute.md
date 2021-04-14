---
description: Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados. Esse atributo se aplica a exemplos de mídia.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Atributo MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502280"
---
# <a name="mfsampleextension_singlefield-attribute"></a><span data-ttu-id="40a59-104">Atributo de MFSampleExtension \_ únicofield</span><span class="sxs-lookup"><span data-stu-id="40a59-104">MFSampleExtension\_SingleField attribute</span></span>

<span data-ttu-id="40a59-105">Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="40a59-105">Specifies whether a video sample contains a single field or two interleaved fields.</span></span> <span data-ttu-id="40a59-106">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="40a59-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="40a59-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="40a59-107">Data type</span></span>

<span data-ttu-id="40a59-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="40a59-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="40a59-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="40a59-109">Get/set</span></span>

<span data-ttu-id="40a59-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="40a59-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="40a59-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="40a59-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="40a59-112">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="40a59-112">Applies to</span></span>

[<span data-ttu-id="40a59-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="40a59-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="40a59-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="40a59-114">Remarks</span></span>

<span data-ttu-id="40a59-115">Se o valor for **true**, o exemplo conterá um campo.</span><span class="sxs-lookup"><span data-stu-id="40a59-115">If the value is **TRUE**, the sample contains one field.</span></span> <span data-ttu-id="40a59-116">Se o valor for **false** ou o atributo não estiver definido, o exemplo conterá um quadro completo.</span><span class="sxs-lookup"><span data-stu-id="40a59-116">If the value is **FALSE** or the attribute is not set, the sample contains a complete frame.</span></span> <span data-ttu-id="40a59-117">(Dois campos se entrelaçados ou um quadro progressivo).</span><span class="sxs-lookup"><span data-stu-id="40a59-117">(Two fields if interlaced, or a progressive frame.)</span></span>

<span data-ttu-id="40a59-118">Se o tipo de mídia for de quadros progressivos ou de campos intercalados, esse atributo deverá ser definido como **falso** ou esquerdo.</span><span class="sxs-lookup"><span data-stu-id="40a59-118">If the media type is progressive frames or interleaved fields, this attribute must be **FALSE** or left unset.</span></span>

<span data-ttu-id="40a59-119">Se o tipo de mídia for um único campo, esse atributo deverá ser **true**.</span><span class="sxs-lookup"><span data-stu-id="40a59-119">If the media type is single field, this attribute must be **TRUE**.</span></span> <span data-ttu-id="40a59-120">Defina o atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) no exemplo para indicar se ele é o campo superior ou o campo inferior.</span><span class="sxs-lookup"><span data-stu-id="40a59-120">Set the [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute on the sample to indicate whether it is the upper field or the lower field.</span></span>

<span data-ttu-id="40a59-121">Atualmente, o processador de vídeo avançado (EVR) não oferece suporte a conteúdo que alterna entre quadros entrelaçados e campos únicos.</span><span class="sxs-lookup"><span data-stu-id="40a59-121">Currently the enhanced video renderer (EVR) does not support content that switches between interlaced frames and single fields.</span></span>

<span data-ttu-id="40a59-122">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="40a59-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a59-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40a59-123">Requirements</span></span>



| <span data-ttu-id="40a59-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a59-124">Requirement</span></span> | <span data-ttu-id="40a59-125">Valor</span><span class="sxs-lookup"><span data-stu-id="40a59-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40a59-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40a59-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40a59-127">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="40a59-127">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="40a59-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40a59-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40a59-129">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="40a59-129">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="40a59-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40a59-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a59-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a59-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a59-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="40a59-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a59-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40a59-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="40a59-134">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="40a59-134">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="40a59-135">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="40a59-135">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="40a59-136">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="40a59-136">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




