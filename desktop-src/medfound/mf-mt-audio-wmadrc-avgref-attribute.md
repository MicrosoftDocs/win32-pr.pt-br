---
description: Nível de volume médio de referência de um arquivo de áudio do Windows Media.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: Atributo MF_MT_AUDIO_WMADRC_AVGREF (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdde0bfb4c2993580d73981e9e121d1f7f18612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165021"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a><span data-ttu-id="d1119-103">\_Atributo MF MT \_ Audio \_ WMADRC \_ AVGREF</span><span class="sxs-lookup"><span data-stu-id="d1119-103">MF\_MT\_AUDIO\_WMADRC\_AVGREF attribute</span></span>

<span data-ttu-id="d1119-104">Nível de volume médio de referência de um arquivo de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d1119-104">Reference average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1119-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d1119-105">Data type</span></span>

<span data-ttu-id="d1119-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d1119-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1119-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1119-107">Remarks</span></span>

<span data-ttu-id="d1119-108">Esse atributo se aplica a tipos de mídia de áudio para codecs de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d1119-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="d1119-109">Especifica o nível de volume médio original do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d1119-109">It specifies the original average volume level of the content.</span></span> <span data-ttu-id="d1119-110">O decodificador pode usar esse valor para executar o controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="d1119-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="d1119-111">O método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) adiciona esse atributo ao tipo de mídia se o cabeçalho ASF contiver o atributo [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) .</span><span class="sxs-lookup"><span data-stu-id="d1119-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) attribute.</span></span> <span data-ttu-id="d1119-112">Esse atributo está documentado na documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d1119-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="d1119-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d1119-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1119-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1119-114">Requirements</span></span>



| <span data-ttu-id="d1119-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1119-115">Requirement</span></span> | <span data-ttu-id="d1119-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d1119-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1119-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1119-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1119-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1119-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d1119-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1119-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1119-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d1119-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d1119-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1119-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1119-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1119-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1119-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1119-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1119-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1119-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1119-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d1119-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d1119-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="d1119-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d1119-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1119-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d1119-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="d1119-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
