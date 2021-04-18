---
description: Contém dados de formato adicionais para um tipo de mídia.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Atributo MF_MT_USER_DATA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791404"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="52dfb-103">\_Atributo de \_ dados de usuário MF MT \_</span><span class="sxs-lookup"><span data-stu-id="52dfb-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="52dfb-104">Contém dados de formato adicionais para um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="52dfb-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="52dfb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="52dfb-105">Data type</span></span>

<span data-ttu-id="52dfb-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="52dfb-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="52dfb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="52dfb-107">Remarks</span></span>

<span data-ttu-id="52dfb-108">O significado dos dados nesse atributo depende do formato descrito pelo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="52dfb-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="52dfb-109">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="52dfb-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="52dfb-110">Dados de formato adicionais</span><span class="sxs-lookup"><span data-stu-id="52dfb-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52dfb-111">Windows Media Codec.</span><span class="sxs-lookup"><span data-stu-id="52dfb-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="52dfb-112">Dados privados do codec.</span><span class="sxs-lookup"><span data-stu-id="52dfb-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="52dfb-113">Estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) convertida.</span><span class="sxs-lookup"><span data-stu-id="52dfb-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="52dfb-114">Dados extras que aparecem após a estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , sem incluir a tabela de cores ou máscaras de cor.</span><span class="sxs-lookup"><span data-stu-id="52dfb-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="52dfb-115">Estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) convertida.</span><span class="sxs-lookup"><span data-stu-id="52dfb-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="52dfb-116">Dados extras que aparecem após a estrutura de formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="52dfb-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="52dfb-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="52dfb-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="52dfb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52dfb-118">Requirements</span></span>



| <span data-ttu-id="52dfb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52dfb-119">Requirement</span></span> | <span data-ttu-id="52dfb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52dfb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52dfb-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52dfb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52dfb-122">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="52dfb-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="52dfb-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52dfb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52dfb-124">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="52dfb-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="52dfb-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52dfb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52dfb-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="52dfb-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52dfb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="52dfb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52dfb-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52dfb-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="52dfb-129">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="52dfb-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="52dfb-130">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="52dfb-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="52dfb-131">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="52dfb-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="52dfb-132">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="52dfb-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
