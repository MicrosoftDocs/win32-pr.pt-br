---
description: Habilita o processamento de vídeo pelo leitor de origem.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Atributo MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461081"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a><span data-ttu-id="44b55-103">\_Leitor de origem MF \_ \_ habilitar atributo de \_ processamento de vídeo \_</span><span class="sxs-lookup"><span data-stu-id="44b55-103">MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="44b55-104">Habilita o processamento de vídeo pelo [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="44b55-104">Enables video processing by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="44b55-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44b55-105">Data type</span></span>

<span data-ttu-id="44b55-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44b55-106">**UINT32**</span></span>



| <span data-ttu-id="44b55-107">Valor</span><span class="sxs-lookup"><span data-stu-id="44b55-107">Value</span></span>                                                                                                                                                                | <span data-ttu-id="44b55-108">Significado</span><span class="sxs-lookup"><span data-stu-id="44b55-108">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <span data-ttu-id="44b55-109"><dt>**Diferente**</dt></span><span class="sxs-lookup"><span data-stu-id="44b55-109"><dt>**Nonzero**</dt></span></span> </dl> | <span data-ttu-id="44b55-110">Habilite o processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="44b55-110">Enable video processing.</span></span><br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <span data-ttu-id="44b55-111"><dt>**Zero**</dt></span><span class="sxs-lookup"><span data-stu-id="44b55-111"><dt>**Zero**</dt></span></span> </dl>             | <span data-ttu-id="44b55-112">Desabilite o processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="44b55-112">Disable video processing.</span></span> <span data-ttu-id="44b55-113">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="44b55-113">(Default)</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="44b55-114">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="44b55-114">Get/set</span></span>

<span data-ttu-id="44b55-115">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="44b55-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="44b55-116">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="44b55-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="44b55-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="44b55-117">Remarks</span></span>

<span data-ttu-id="44b55-118">Se esse atributo for **true** (diferente de zero), o leitor de origem poderá executar o seguinte processamento de vídeo limitado em quadros de vídeo descompactados:</span><span class="sxs-lookup"><span data-stu-id="44b55-118">If this attribute is **TRUE** (nonzero), the source reader can perform the following limited video processing on uncompressed video frames:</span></span>

-   <span data-ttu-id="44b55-119">Conversão de YUV para RGB-32.</span><span class="sxs-lookup"><span data-stu-id="44b55-119">Conversion from YUV to RGB-32.</span></span>
-   <span data-ttu-id="44b55-120">Desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="44b55-120">Deinterlacing.</span></span>

<span data-ttu-id="44b55-121">Essas operações são executadas no software e não são otimizadas para reprodução.</span><span class="sxs-lookup"><span data-stu-id="44b55-121">These operations are performed in software, and are not optimized for playback.</span></span> <span data-ttu-id="44b55-122">Esse recurso destina-se a aplicativos que processam um pequeno número de quadros, por exemplo, para criar uma miniatura de vídeo — ou aplicativos que não decodificam quadros em tempo real.</span><span class="sxs-lookup"><span data-stu-id="44b55-122">This feature is intended for applications that process a small number of frames—for example, to create a video thumbnail—or applications that do not decode frames in real time.</span></span> <span data-ttu-id="44b55-123">A operação de desentrelaçamento interpola os dados de um único campo, portanto, ele tem perda.</span><span class="sxs-lookup"><span data-stu-id="44b55-123">The deinterlace operation interpolates data from a single field, so it is lossy.</span></span>

<span data-ttu-id="44b55-124">Evite essa configuração se você estiver usando o Direct3D para exibir os quadros de vídeo, pois a GPU geralmente fornece melhores recursos de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="44b55-124">Avoid this setting if you are using Direct3D to display the video frames, because the GPU generally provides better video processing capabilities.</span></span>

<span data-ttu-id="44b55-125">Se esse atributo for **true**, os seguintes atributos deverão ser **falsos**:</span><span class="sxs-lookup"><span data-stu-id="44b55-125">If this attribute is **TRUE**, the following attributes must be **FALSE**:</span></span>

-   [<span data-ttu-id="44b55-126">\_Gerenciador de \_ D3D do leitor de origem MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="44b55-126">MF\_SOURCE\_READER\_D3D\_MANAGER</span></span>](mf-source-reader-d3d-manager.md)
-   [<span data-ttu-id="44b55-127">\_conversores do MF ReadWrite \_ Disable \_</span><span class="sxs-lookup"><span data-stu-id="44b55-127">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)

## <a name="requirements"></a><span data-ttu-id="44b55-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b55-128">Requirements</span></span>



| <span data-ttu-id="44b55-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b55-129">Requirement</span></span> | <span data-ttu-id="44b55-130">Valor</span><span class="sxs-lookup"><span data-stu-id="44b55-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b55-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b55-131">Minimum supported client</span></span><br/> | <span data-ttu-id="44b55-132">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44b55-132">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="44b55-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b55-133">Minimum supported server</span></span><br/> | <span data-ttu-id="44b55-134">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="44b55-134">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44b55-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44b55-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="44b55-136"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b55-136"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b55-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="44b55-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b55-138">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44b55-138">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44b55-139">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="44b55-139">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="44b55-140">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="44b55-140">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




