---
description: Bloquear alinhamento, em bytes, para um tipo de mídia de áudio. O alinhamento de bloco é a unidade atômica mínima de dados para o formato de áudio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Atributo MF_MT_AUDIO_BLOCK_ALIGNMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771512"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="52f35-104">\_Atributo de \_ alinhamento de bloco de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="52f35-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="52f35-105">Bloquear alinhamento, em bytes, para um tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="52f35-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="52f35-106">O alinhamento de bloco é a unidade atômica mínima de dados para o formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="52f35-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="52f35-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="52f35-107">Data type</span></span>

<span data-ttu-id="52f35-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="52f35-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="52f35-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="52f35-109">Remarks</span></span>

<span data-ttu-id="52f35-110">Para formatos de áudio PCM, o alinhamento de bloco é igual ao número de canais de áudio multiplicado pelo número de bytes por amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="52f35-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="52f35-111">Esse atributo corresponde ao membro **nBlockAlign** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="52f35-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="52f35-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="52f35-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f35-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f35-113">Requirements</span></span>



| <span data-ttu-id="52f35-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f35-114">Requirement</span></span> | <span data-ttu-id="52f35-115">Valor</span><span class="sxs-lookup"><span data-stu-id="52f35-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52f35-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f35-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52f35-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="52f35-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="52f35-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f35-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52f35-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="52f35-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="52f35-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52f35-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f35-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f35-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f35-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f35-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f35-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52f35-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52f35-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="52f35-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="52f35-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="52f35-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="52f35-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="52f35-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="52f35-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="52f35-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
