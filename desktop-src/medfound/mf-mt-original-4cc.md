---
description: Contém o codec original FOURCC para um fluxo de vídeo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Atributo MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922393"
---
# <a name="mf_mt_original_4cc-attribute"></a><span data-ttu-id="ceea0-103">\_Atributo 4cc do MF MT \_ original \_</span><span class="sxs-lookup"><span data-stu-id="ceea0-103">MF\_MT\_ORIGINAL\_4CC attribute</span></span>

<span data-ttu-id="ceea0-104">Contém o codec original FOURCC para um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ceea0-104">Contains the original codec FOURCC for a video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="ceea0-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ceea0-105">Data type</span></span>

<span data-ttu-id="ceea0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ceea0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ceea0-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="ceea0-107">Get/set</span></span>

<span data-ttu-id="ceea0-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ceea0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ceea0-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ceea0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ceea0-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="ceea0-110">Applies to</span></span>

[<span data-ttu-id="ceea0-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ceea0-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="ceea0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceea0-112">Remarks</span></span>

<span data-ttu-id="ceea0-113">Dependendo do arquivo de origem, a origem da mídia AVI pode definir esse atributo nos tipos de mídia que ele oferece.</span><span class="sxs-lookup"><span data-stu-id="ceea0-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="ceea0-114">Um arquivo AVI contém um cabeçalho de fluxo para cada fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ceea0-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="ceea0-115">A fonte de mídia AVI converte o cabeçalho do fluxo em um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="ceea0-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="ceea0-116">Para fluxos de vídeo compactados, o cabeçalho de fluxo contém um FOURCC que identifica o codec de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ceea0-116">For compressed video streams, the stream header contains a FOURCC that identifies the video codec.</span></span> <span data-ttu-id="ceea0-117">Na maioria dos casos, a origem de mídia AVI converte esse FOURCC diretamente em um GUID de subtipo, conforme descrito no tópico [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ceea0-117">In most cases, the AVI media source converts this FOURCC directly to a subtype GUID, as described in the topic [Video Subtype GUIDs](video-subtype-guids.md).</span></span> <span data-ttu-id="ceea0-118">Em alguns casos, no entanto, ele mapeia o FOURCC original para outro FOURCC que é equivalente.</span><span class="sxs-lookup"><span data-stu-id="ceea0-118">In some cases, however, it maps the original FOURCC to another FOURCC that is equivalent.</span></span> <span data-ttu-id="ceea0-119">Nesse caso, a origem da mídia armazena o FOURCC original no tipo de mídia, usando o \_ atributo 4cc do MF MT \_ original \_ .</span><span class="sxs-lookup"><span data-stu-id="ceea0-119">If so, the media source stores the original FOURCC in the media type, using the MF\_MT\_ORIGINAL\_4CC attribute.</span></span>

<span data-ttu-id="ceea0-120">Os mapeamentos FOURCC são armazenados no registro sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="ceea0-120">The FOURCC mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="ceea0-121">**HKEY \_ CLASSES \_ raiz** \\ **MediaFoundation** \\ **MapVideo4cc**</span><span class="sxs-lookup"><span data-stu-id="ceea0-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapVideo4cc**</span></span>

<span data-ttu-id="ceea0-122">Cada entrada é um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ceea0-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="ceea0-123">O nome da entrada é a representação hexadecimal do FOURCC, sem um prefixo "0x", e com o primeiro caractere exibido primeiro na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ceea0-123">The name of the entry is the hexadecimal representation of the FOURCC, without an "0x" prefix, and with the first character appearing first in the string.</span></span> <span data-ttu-id="ceea0-124">Por exemplo, o código FOURCC ' ABCD ' apareceria como "61626364".</span><span class="sxs-lookup"><span data-stu-id="ceea0-124">For example, the FOURCC code 'abcd' would appear as "61626364".</span></span> <span data-ttu-id="ceea0-125">O valor da entrada é o código FOURCC equivalente.</span><span class="sxs-lookup"><span data-stu-id="ceea0-125">The value of the entry is the equivalent FOURCC code.</span></span>

<span data-ttu-id="ceea0-126">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ceea0-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceea0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceea0-127">Requirements</span></span>



| <span data-ttu-id="ceea0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceea0-128">Requirement</span></span> | <span data-ttu-id="ceea0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ceea0-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ceea0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceea0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ceea0-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ceea0-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ceea0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceea0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ceea0-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ceea0-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ceea0-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ceea0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceea0-135"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceea0-135"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceea0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceea0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceea0-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ceea0-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ceea0-138">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="ceea0-138">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




