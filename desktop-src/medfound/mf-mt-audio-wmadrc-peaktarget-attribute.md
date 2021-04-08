---
description: Nível de volume de pico de destino de um arquivo de áudio do Windows Media.
ms.assetid: 73f4e763-dcb7-48cd-ab80-37635d973da0
title: Atributo MF_MT_AUDIO_WMADRC_PEAKTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48391adfaa19dcc00ea4d7a30b909b4573f67222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922394"
---
# <a name="mf_mt_audio_wmadrc_peaktarget-attribute"></a><span data-ttu-id="19a51-103">\_Atributo MF MT \_ Audio \_ WMADRC \_ PEAKTARGET</span><span class="sxs-lookup"><span data-stu-id="19a51-103">MF\_MT\_AUDIO\_WMADRC\_PEAKTARGET attribute</span></span>

<span data-ttu-id="19a51-104">Nível de volume de pico de destino de um arquivo de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="19a51-104">Target peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="19a51-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19a51-105">Data type</span></span>

<span data-ttu-id="19a51-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19a51-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19a51-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="19a51-107">Remarks</span></span>

<span data-ttu-id="19a51-108">Esse atributo se aplica a tipos de mídia de áudio para codecs de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="19a51-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="19a51-109">Especifica o nível de volume de pico de destino do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="19a51-109">It specifies the target peak volume level of the content.</span></span> <span data-ttu-id="19a51-110">O decodificador pode usar esse valor para executar o controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="19a51-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="19a51-111">O método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) adiciona esse atributo ao tipo de mídia se o cabeçalho ASF contiver o atributo [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) .</span><span class="sxs-lookup"><span data-stu-id="19a51-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakTarget**](../wmformat/wm-wmadrcpeaktarget.md) attribute.</span></span> <span data-ttu-id="19a51-112">Esse atributo está documentado na documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="19a51-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="19a51-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="19a51-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a51-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19a51-114">Requirements</span></span>



| <span data-ttu-id="19a51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a51-115">Requirement</span></span> | <span data-ttu-id="19a51-116">Valor</span><span class="sxs-lookup"><span data-stu-id="19a51-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19a51-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19a51-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="19a51-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="19a51-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19a51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19a51-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19a51-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="19a51-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19a51-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="19a51-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a51-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a51-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="19a51-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a51-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19a51-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19a51-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19a51-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19a51-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="19a51-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19a51-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="19a51-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="19a51-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="19a51-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
