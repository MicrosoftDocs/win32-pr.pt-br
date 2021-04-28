---
description: Atributo MF_MT_AUDIO_SAMPLES_PER_SECOND-número de amostras de áudio por segundo em um tipo de mídia de áudio.
ms.assetid: f640016d-595e-4b20-8ce8-23a029c2b064
title: Atributo MF_MT_AUDIO_SAMPLES_PER_SECOND (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a91b44ba4c55bf2512eefddfe3bc7a18d2eddd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093094"
---
# <a name="mf_mt_audio_samples_per_second-attribute"></a><span data-ttu-id="e24cf-103">\_Atributo de amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="e24cf-103">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="e24cf-104">Número de amostras de áudio por segundo em um tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="e24cf-104">Number of audio samples per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e24cf-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e24cf-105">Data type</span></span>

<span data-ttu-id="e24cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e24cf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e24cf-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e24cf-107">Remarks</span></span>

<span data-ttu-id="e24cf-108">Esse atributo corresponde ao membro **nSamplesPerSec** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e24cf-108">This attribute corresponds to the **nSamplesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="e24cf-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e24cf-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24cf-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24cf-110">Requirements</span></span>



| <span data-ttu-id="e24cf-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24cf-111">Requirement</span></span> | <span data-ttu-id="e24cf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e24cf-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e24cf-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24cf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e24cf-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="e24cf-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e24cf-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e24cf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e24cf-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e24cf-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e24cf-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e24cf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24cf-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24cf-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24cf-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e24cf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24cf-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e24cf-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e24cf-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e24cf-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e24cf-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e24cf-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e24cf-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e24cf-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e24cf-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="e24cf-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="e24cf-125">**\_ \_ amostras float de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="e24cf-125">**MF\_MT\_AUDIO\_FLOAT\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-float-samples-per-second-attribute.md)
</dt> </dl>

 

 
