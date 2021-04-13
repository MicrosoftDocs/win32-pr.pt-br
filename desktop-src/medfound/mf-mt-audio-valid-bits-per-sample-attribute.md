---
description: Número de bits válidos de dados de áudio em cada amostra de áudio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Atributo MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297633"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="81a28-103">\_Áudio MF \_ MT \_ \_ bits válidos \_ por \_ exemplo de atributo</span><span class="sxs-lookup"><span data-stu-id="81a28-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="81a28-104">Número de bits válidos de dados de áudio em cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="81a28-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="81a28-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="81a28-105">Data type</span></span>

<span data-ttu-id="81a28-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="81a28-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="81a28-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="81a28-107">Remarks</span></span>

<span data-ttu-id="81a28-108">O exemplo de **\_ áudio MF mt de \_ \_ \_ bits \_ por \_ amostra** é usado para formatos de áudio que contêm preenchimento após cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="81a28-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="81a28-109">O tamanho total de cada amostra de áudio, incluindo bits de preenchimento, é fornecido no atributo [**MF \_ MT \_ Audio \_ bits \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="81a28-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="81a28-110">Se o **atributo \_ áudio MF MT \_ \_ válido \_ bits \_ por \_ exemplo** não estiver definido, use o atributo [**MF \_ MT \_ Audio \_ bits \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) para localizar o número de bits válidos por amostra.</span><span class="sxs-lookup"><span data-stu-id="81a28-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="81a28-111">Se um formato de áudio não contiver nenhum bits de preenchimento, esse atributo não deverá ser definido ou deverá ser definido com o mesmo valor que o [**\_ exemplo de bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="81a28-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="81a28-112">Esse atributo corresponde ao membro **wValidBitsPerSample** da estrutura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="81a28-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="81a28-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="81a28-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a28-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a28-114">Requirements</span></span>



| <span data-ttu-id="81a28-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a28-115">Requirement</span></span> | <span data-ttu-id="81a28-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81a28-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81a28-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81a28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81a28-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="81a28-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="81a28-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81a28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81a28-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81a28-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="81a28-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81a28-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a28-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a28-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a28-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="81a28-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a28-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81a28-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81a28-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="81a28-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="81a28-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="81a28-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="81a28-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="81a28-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="81a28-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="81a28-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
