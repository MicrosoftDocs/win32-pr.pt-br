---
description: Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Atributo MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502386"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="2715d-103">\_Áudio MF \_ MT \_ prefira \_ atributo WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="2715d-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="2715d-104">Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="2715d-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="2715d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2715d-105">Data type</span></span>

<span data-ttu-id="2715d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2715d-106">**UINT32**</span></span>

<span data-ttu-id="2715d-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="2715d-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2715d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2715d-108">Remarks</span></span>

<span data-ttu-id="2715d-109">Esse atributo fornece uma dica para a função [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="2715d-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="2715d-110">Se o atributo for **true**, a função converterá o tipo de mídia de áudio em uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) sempre que possível, em vez de convertê-lo em uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2715d-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="2715d-111">A função [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) define esse atributo.</span><span class="sxs-lookup"><span data-stu-id="2715d-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="2715d-112">Você pode substituir o valor desse atributo, mas a definição desse atributo como **true** não garante que um tipo de mídia de áudio possa ser convertido em um formulário [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2715d-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="2715d-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2715d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2715d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2715d-114">Requirements</span></span>



| <span data-ttu-id="2715d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2715d-115">Requirement</span></span> | <span data-ttu-id="2715d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2715d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2715d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2715d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2715d-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="2715d-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="2715d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2715d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2715d-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2715d-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2715d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2715d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2715d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2715d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2715d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2715d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2715d-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2715d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2715d-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2715d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2715d-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="2715d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2715d-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="2715d-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="2715d-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="2715d-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
