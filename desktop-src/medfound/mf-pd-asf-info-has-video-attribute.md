---
description: Especifica se um arquivo ASF (Advanced Systems Format) contém pelo menos um fluxo de vídeo.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: Atributo MF_PD_ASF_INFO_HAS_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802096"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="80bc9-103">\_Informações ASF do MF PD \_ \_ \_ têm atributo de \_ vídeo</span><span class="sxs-lookup"><span data-stu-id="80bc9-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="80bc9-104">Especifica se um arquivo ASF (Advanced Systems Format) contém pelo menos um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="80bc9-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="80bc9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="80bc9-105">Data type</span></span>

<span data-ttu-id="80bc9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-106">**UINT32**</span></span>

<span data-ttu-id="80bc9-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="80bc9-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80bc9-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="80bc9-108">Remarks</span></span>

<span data-ttu-id="80bc9-109">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="80bc9-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="80bc9-110">Se o valor for **true**, o arquivo terá pelo menos um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="80bc9-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="80bc9-111">Caso contrário, o arquivo não contém fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="80bc9-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="80bc9-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="80bc9-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="80bc9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80bc9-113">Requirements</span></span>



| <span data-ttu-id="80bc9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="80bc9-114">Requirement</span></span> | <span data-ttu-id="80bc9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="80bc9-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bc9-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80bc9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80bc9-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80bc9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80bc9-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80bc9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80bc9-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80bc9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="80bc9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80bc9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80bc9-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="80bc9-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80bc9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="80bc9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bc9-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80bc9-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80bc9-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="80bc9-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="80bc9-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="80bc9-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="80bc9-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="80bc9-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="80bc9-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="80bc9-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




