---
description: Especifica para um tipo de mídia se cada amostra é independente dos outros exemplos no fluxo.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: Atributo MF_MT_ALL_SAMPLES_INDEPENDENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748083"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="c2088-103">\_ \_ Atributo independente de todos os \_ exemplos \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="c2088-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="c2088-104">Especifica para um tipo de mídia se cada amostra é independente dos outros exemplos no fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2088-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2088-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c2088-105">Data type</span></span>

<span data-ttu-id="c2088-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2088-106">**UINT32**</span></span>

<span data-ttu-id="c2088-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c2088-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2088-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2088-108">Remarks</span></span>

<span data-ttu-id="c2088-109">Se esse atributo for **false**, alguns exemplos não poderão ser usados sem fazer referência a outros exemplos no fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2088-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="c2088-110">Por exemplo, se um formato de vídeo contiver quadros Delta, esse atributo deverá ser **false**.</span><span class="sxs-lookup"><span data-stu-id="c2088-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="c2088-111">Esse atributo corresponde ao campo **bTemporalCompression** na estrutura do [**tipo de \_ mídia \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) do DirectShow am.</span><span class="sxs-lookup"><span data-stu-id="c2088-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="c2088-112">Defina esse atributo como **true** para todos os tipos de mídia descompactados.</span><span class="sxs-lookup"><span data-stu-id="c2088-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="c2088-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c2088-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2088-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2088-114">Requirements</span></span>



| <span data-ttu-id="c2088-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2088-115">Requirement</span></span> | <span data-ttu-id="c2088-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c2088-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2088-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2088-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c2088-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c2088-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c2088-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2088-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c2088-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c2088-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c2088-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2088-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2088-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2088-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2088-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2088-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2088-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2088-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2088-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c2088-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c2088-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c2088-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c2088-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c2088-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c2088-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c2088-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
