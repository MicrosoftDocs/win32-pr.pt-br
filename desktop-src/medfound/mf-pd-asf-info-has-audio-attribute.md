---
description: Especifica se um arquivo ASF (Advanced Systems Format) contém fluxos de áudio.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: Atributo MF_PD_ASF_INFO_HAS_AUDIO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e2fbf9698e470af92cbd21fc5f26883dc5fd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170515"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a><span data-ttu-id="98e7a-103">As \_ informações do MF PD \_ ASF \_ têm o \_ \_ atributo Audio</span><span class="sxs-lookup"><span data-stu-id="98e7a-103">MF\_PD\_ASF\_INFO\_HAS\_AUDIO attribute</span></span>

<span data-ttu-id="98e7a-104">Especifica se um arquivo ASF (Advanced Systems Format) contém fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="98e7a-104">Specifies whether an Advanced Systems Format (ASF) file contains any audio streams.</span></span>

## <a name="data-type"></a><span data-ttu-id="98e7a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="98e7a-105">Data type</span></span>

<span data-ttu-id="98e7a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="98e7a-106">**UINT32**</span></span>

<span data-ttu-id="98e7a-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="98e7a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e7a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="98e7a-108">Remarks</span></span>

<span data-ttu-id="98e7a-109">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="98e7a-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="98e7a-110">Se o valor for **true**, o arquivo terá pelo menos um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="98e7a-110">If the value is **TRUE**, the file has at least one audio stream.</span></span> <span data-ttu-id="98e7a-111">Caso contrário, o arquivo não contém fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="98e7a-111">Otherwise, the file does not contain any audio streams.</span></span>

<span data-ttu-id="98e7a-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="98e7a-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e7a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98e7a-113">Requirements</span></span>



| <span data-ttu-id="98e7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="98e7a-114">Requirement</span></span> | <span data-ttu-id="98e7a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="98e7a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e7a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98e7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="98e7a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98e7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="98e7a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98e7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="98e7a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98e7a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="98e7a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98e7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e7a-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e7a-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e7a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="98e7a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e7a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98e7a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="98e7a-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="98e7a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="98e7a-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="98e7a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="98e7a-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="98e7a-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="98e7a-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="98e7a-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="98e7a-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="98e7a-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




