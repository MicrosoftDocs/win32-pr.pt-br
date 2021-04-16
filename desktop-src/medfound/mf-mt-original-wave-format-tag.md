---
description: Contém a marca de formato WAVE original para um fluxo de áudio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: Atributo MF_MT_ORIGINAL_WAVE_FORMAT_TAG (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786951"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="836b8-103">\_Atributo de \_ \_ marca de \_ formato wave original MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="836b8-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="836b8-104">Contém a marca de formato WAVE original para um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="836b8-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="836b8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="836b8-105">Data type</span></span>

<span data-ttu-id="836b8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="836b8-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="836b8-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="836b8-107">Get/set</span></span>

<span data-ttu-id="836b8-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="836b8-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="836b8-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="836b8-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="836b8-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="836b8-110">Applies to</span></span>

[<span data-ttu-id="836b8-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="836b8-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="836b8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="836b8-112">Remarks</span></span>

<span data-ttu-id="836b8-113">Dependendo do arquivo de origem, a origem da mídia AVI pode definir esse atributo nos tipos de mídia que ele oferece.</span><span class="sxs-lookup"><span data-stu-id="836b8-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="836b8-114">Um arquivo AVI contém um cabeçalho de fluxo para cada fluxo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="836b8-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="836b8-115">A fonte de mídia AVI converte o cabeçalho do fluxo em um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="836b8-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="836b8-116">Para fluxos de áudio, o cabeçalho de fluxo contém uma marca de formato que identifica o formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="836b8-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="836b8-117">(A marca de formato está contida no membro **wFormatTag** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .) Na maioria dos casos, a origem de mídia AVI converte a marca de formato diretamente em um GUID de subtipo, conforme descrito no tópico [**GUIDs de subtipo de áudio**](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="836b8-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="836b8-118">Em alguns casos, no entanto, ele mapeia a marca de formato original para outra marca de formato equivalente.</span><span class="sxs-lookup"><span data-stu-id="836b8-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="836b8-119">Nesse caso, a origem da mídia armazena a marca de formato original no tipo de mídia, usando \_ o \_ atributo de marca de formato wave original MF MT \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="836b8-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="836b8-120">Os mapeamentos de formato são armazenados no registro sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="836b8-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="836b8-121">**HKEY \_ CLASSES \_ raiz** \\ **MediaFoundation** \\ **MapAudioFormatTag**</span><span class="sxs-lookup"><span data-stu-id="836b8-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="836b8-122">Cada entrada é um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="836b8-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="836b8-123">O nome da entrada é a representação decimal da marca de formato.</span><span class="sxs-lookup"><span data-stu-id="836b8-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="836b8-124">O valor da entrada é a marca de formato equivalente.</span><span class="sxs-lookup"><span data-stu-id="836b8-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="836b8-125">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="836b8-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="836b8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="836b8-126">Requirements</span></span>



| <span data-ttu-id="836b8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="836b8-127">Requirement</span></span> | <span data-ttu-id="836b8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="836b8-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="836b8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="836b8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="836b8-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="836b8-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="836b8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="836b8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="836b8-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="836b8-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="836b8-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="836b8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="836b8-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="836b8-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836b8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="836b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836b8-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="836b8-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="836b8-137">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="836b8-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
