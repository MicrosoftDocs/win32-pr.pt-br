---
description: Nível de volume médio de destino de um arquivo de áudio do Windows Media.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: Atributo MF_MT_AUDIO_WMADRC_AVGTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297475"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a><span data-ttu-id="78ecd-103">\_Atributo MF MT \_ Audio \_ WMADRC \_ AVGTARGET</span><span class="sxs-lookup"><span data-stu-id="78ecd-103">MF\_MT\_AUDIO\_WMADRC\_AVGTARGET attribute</span></span>

<span data-ttu-id="78ecd-104">Nível de volume médio de destino de um arquivo de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="78ecd-104">Target average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="78ecd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="78ecd-105">Data type</span></span>

<span data-ttu-id="78ecd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="78ecd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="78ecd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="78ecd-107">Remarks</span></span>

<span data-ttu-id="78ecd-108">Esse atributo se aplica a tipos de mídia de áudio para codecs de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="78ecd-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="78ecd-109">Especifica o nível de volume médio de destino do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="78ecd-109">It specifies the target average volume level of the content.</span></span> <span data-ttu-id="78ecd-110">O decodificador pode usar esse valor para executar o controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="78ecd-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="78ecd-111">O método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) adiciona esse atributo ao tipo de mídia se o cabeçalho ASF contiver o atributo [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) .</span><span class="sxs-lookup"><span data-stu-id="78ecd-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) attribute.</span></span> <span data-ttu-id="78ecd-112">Esse atributo está documentado na documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="78ecd-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="78ecd-113">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="78ecd-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="78ecd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78ecd-114">Requirements</span></span>



| <span data-ttu-id="78ecd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ecd-115">Requirement</span></span> | <span data-ttu-id="78ecd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="78ecd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78ecd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78ecd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78ecd-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="78ecd-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="78ecd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78ecd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78ecd-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="78ecd-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="78ecd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78ecd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="78ecd-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ecd-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78ecd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="78ecd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ecd-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78ecd-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="78ecd-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="78ecd-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="78ecd-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="78ecd-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="78ecd-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="78ecd-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="78ecd-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="78ecd-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
