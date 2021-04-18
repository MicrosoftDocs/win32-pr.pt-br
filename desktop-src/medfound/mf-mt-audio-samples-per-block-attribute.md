---
description: Número de amostras de áudio contidas em um bloco compactado de dados de áudio. Esse atributo pode ser usado em formatos de áudio compactados que têm um número fixo de amostras dentro de cada bloco.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Atributo MF_MT_AUDIO_SAMPLES_PER_BLOCK (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780435"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="304fc-104">\_Exemplos de áudio MF MT \_ \_ \_ por atributo de \_ bloco</span><span class="sxs-lookup"><span data-stu-id="304fc-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="304fc-105">Número de amostras de áudio contidas em um bloco compactado de dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="304fc-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="304fc-106">Esse atributo pode ser usado em formatos de áudio compactados que têm um número fixo de amostras dentro de cada bloco.</span><span class="sxs-lookup"><span data-stu-id="304fc-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="304fc-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="304fc-107">Data type</span></span>

<span data-ttu-id="304fc-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="304fc-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="304fc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="304fc-109">Remarks</span></span>

<span data-ttu-id="304fc-110">Esse atributo corresponde ao membro **wSamplesPerBlock** da estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="304fc-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="304fc-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="304fc-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="304fc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="304fc-112">Requirements</span></span>



| <span data-ttu-id="304fc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="304fc-113">Requirement</span></span> | <span data-ttu-id="304fc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="304fc-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="304fc-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="304fc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="304fc-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="304fc-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="304fc-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="304fc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="304fc-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="304fc-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="304fc-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="304fc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="304fc-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="304fc-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="304fc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="304fc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304fc-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="304fc-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="304fc-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="304fc-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="304fc-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="304fc-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="304fc-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="304fc-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="304fc-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="304fc-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
