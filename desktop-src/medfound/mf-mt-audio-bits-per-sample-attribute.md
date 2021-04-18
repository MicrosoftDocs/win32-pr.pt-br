---
description: Número de bits por amostra de áudio em um tipo de mídia de áudio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Atributo MF_MT_AUDIO_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781113"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="8aec6-103">\_Bits de áudio MF MT \_ \_ \_ por exemplo de \_ atributo</span><span class="sxs-lookup"><span data-stu-id="8aec6-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="8aec6-104">Número de bits por amostra de áudio em um tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="8aec6-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="8aec6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8aec6-105">Data type</span></span>

<span data-ttu-id="8aec6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8aec6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8aec6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aec6-107">Remarks</span></span>

<span data-ttu-id="8aec6-108">Esse atributo corresponde ao membro **wBitsPerSample** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8aec6-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="8aec6-109">Se alguns bits contiverem o preenchimento, defina o [**\_ áudio MF MT \_ Audio \_ válido \_ \_ por \_ exemplo**](mf-mt-audio-valid-bits-per-sample-attribute.md) para especificar o número de bits de dados de áudio válidos em cada amostra.</span><span class="sxs-lookup"><span data-stu-id="8aec6-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="8aec6-110">Se o áudio contiver 8 bits por amostra, os exemplos de áudio serão valores não assinados.</span><span class="sxs-lookup"><span data-stu-id="8aec6-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="8aec6-111">(Cada amostra de áudio tem o intervalo de 0 a 255.) Se o áudio contiver 16 bits por amostra ou superior, os exemplos de áudio serão valores assinados.</span><span class="sxs-lookup"><span data-stu-id="8aec6-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="8aec6-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8aec6-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aec6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aec6-113">Requirements</span></span>



| <span data-ttu-id="8aec6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aec6-114">Requirement</span></span> | <span data-ttu-id="8aec6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8aec6-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8aec6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aec6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8aec6-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="8aec6-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8aec6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aec6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8aec6-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8aec6-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8aec6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8aec6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aec6-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aec6-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aec6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8aec6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aec6-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aec6-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8aec6-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8aec6-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8aec6-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="8aec6-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8aec6-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="8aec6-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="8aec6-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="8aec6-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
