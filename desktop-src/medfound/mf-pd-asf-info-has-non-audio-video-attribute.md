---
description: Especifica se um arquivo ASF (Advanced Systems Format) contém todos os fluxos que não são áudio ou vídeo.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: Atributo MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922172"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="c0138-103">As \_ informações do MF PD \_ ASF \_ têm um atributo de \_ \_ \_ vídeo sem áudio \_</span><span class="sxs-lookup"><span data-stu-id="c0138-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="c0138-104">Especifica se um arquivo ASF (Advanced Systems Format) contém todos os fluxos que não são áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0138-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="c0138-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c0138-105">Data type</span></span>

<span data-ttu-id="c0138-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c0138-106">**UINT32**</span></span>

<span data-ttu-id="c0138-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c0138-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0138-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0138-108">Remarks</span></span>

<span data-ttu-id="c0138-109">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="c0138-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="c0138-110">Se o valor for **true**, o arquivo terá pelo menos um fluxo que não seja áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0138-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="c0138-111">Os exemplos incluem fluxos de imagem, comandos de script e dados arbitrários personalizados.</span><span class="sxs-lookup"><span data-stu-id="c0138-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="c0138-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="c0138-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0138-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0138-113">Requirements</span></span>



| <span data-ttu-id="c0138-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0138-114">Requirement</span></span> | <span data-ttu-id="c0138-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c0138-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0138-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0138-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0138-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0138-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c0138-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0138-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0138-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0138-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0138-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0138-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0138-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0138-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0138-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0138-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0138-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0138-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c0138-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c0138-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c0138-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c0138-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c0138-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c0138-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c0138-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="c0138-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c0138-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="c0138-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




