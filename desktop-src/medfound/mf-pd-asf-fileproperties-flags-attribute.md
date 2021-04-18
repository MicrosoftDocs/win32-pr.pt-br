---
description: Especifica se um arquivo ASF (Advanced Systems Format) é difundido ou pesquisável. Esse valor corresponde ao campo Flags do objeto de propriedades File, definido na especificação do ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Atributo MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751023"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="2dd6c-104">\_Atributo de \_ \_ sinalizadores FileProperties do MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="2dd6c-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="2dd6c-105">Especifica se um arquivo ASF (Advanced Systems Format) é difundido ou pesquisável.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="2dd6c-106">Esse valor corresponde ao campo Flags do objeto de propriedades File, definido na especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2dd6c-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2dd6c-107">Data type</span></span>

<span data-ttu-id="2dd6c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2dd6c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dd6c-109">Remarks</span></span>

<span data-ttu-id="2dd6c-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="2dd6c-111">O valor do atributo é uma operação OR dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="2dd6c-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="2dd6c-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="2dd6c-112">Flag</span></span> | <span data-ttu-id="2dd6c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2dd6c-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd6c-114">0x01</span><span class="sxs-lookup"><span data-stu-id="2dd6c-114">0x01</span></span> | <span data-ttu-id="2dd6c-115">Sinalizador de difusão.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-115">Broadcast flag.</span></span> <span data-ttu-id="2dd6c-116">O arquivo está em processo de criação.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="2dd6c-117">0x02</span><span class="sxs-lookup"><span data-stu-id="2dd6c-117">0x02</span></span> | <span data-ttu-id="2dd6c-118">Sinalizador pesquisável.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-118">Seekable flag.</span></span> <span data-ttu-id="2dd6c-119">O arquivo é pesquisável.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-119">The file is seekable.</span></span><br/> <span data-ttu-id="2dd6c-120">Um arquivo será pesquisável se um fluxo de áudio estiver presente e o tamanho máximo do pacote de dados for igual ao tamanho mínimo do pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="2dd6c-121">Ele também pode ser pesquisável se o arquivo tiver um fluxo de áudio e um fluxo de vídeo com um objeto de índice simples correspondente.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="2dd6c-122">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="2dd6c-123">Se o sinalizador de difusão for definido, os seguintes atributos no descritor de apresentação não serão válidos:</span><span class="sxs-lookup"><span data-stu-id="2dd6c-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="2dd6c-124">**\_ID do \_ \_ arquivo FileProperties \_ do MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="2dd6c-125">**\_hora de \_ \_ criação de FileProperties do \_ MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="2dd6c-126">**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="2dd6c-127">**\_duração da \_ \_ reprodução de FileProperties do \_ MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="2dd6c-128">**\_duração de \_ \_ envio de FileProperties do \_ MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="2dd6c-129">Além disso, os valores de atributo de [**\_ \_ \_ \_ \_ \_ tamanho**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) máximo de pacote FileProperties e MF PD ASF do [**MF \_ PD \_ \_ \_ \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) são definidos como o tamanho real do pacote.</span><span class="sxs-lookup"><span data-stu-id="2dd6c-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd6c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dd6c-130">Requirements</span></span>



| <span data-ttu-id="2dd6c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd6c-131">Requirement</span></span> | <span data-ttu-id="2dd6c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2dd6c-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd6c-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dd6c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd6c-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dd6c-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2dd6c-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dd6c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd6c-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2dd6c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2dd6c-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dd6c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dd6c-138"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd6c-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd6c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dd6c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd6c-140">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2dd6c-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dd6c-141">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2dd6c-142">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2dd6c-143">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2dd6c-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2dd6c-144">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="2dd6c-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2dd6c-145">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2dd6c-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2dd6c-146">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="2dd6c-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




