---
description: Especifica o tamanho médio do buffer necessário para um arquivo de formato de protocolo ASF (taxa de bits variável) (VBR).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: Atributo MF_PD_ASF_METADATA_V8_BUFFERAVERAGE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814551"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="a03e6-103">\_Atributo MF PD \_ ASF \_ Metadata \_ V8 \_ BUFFERAVERAGE</span><span class="sxs-lookup"><span data-stu-id="a03e6-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="a03e6-104">Especifica o tamanho médio do buffer necessário para um arquivo de formato de protocolo ASF (taxa de bits variável) (VBR).</span><span class="sxs-lookup"><span data-stu-id="a03e6-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a03e6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a03e6-105">Data type</span></span>

<span data-ttu-id="a03e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a03e6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a03e6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a03e6-107">Remarks</span></span>

<span data-ttu-id="a03e6-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="a03e6-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a03e6-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo que se aplica ao descritor de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="a03e6-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="a03e6-110">Esse atributo aplica-se somente a arquivos criados pela versão 8 do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a03e6-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="a03e6-111">Ele corresponde ao atributo **BufferAverage** no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="a03e6-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a03e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a03e6-112">Requirements</span></span>



| <span data-ttu-id="a03e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a03e6-113">Requirement</span></span> | <span data-ttu-id="a03e6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a03e6-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a03e6-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a03e6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a03e6-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a03e6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a03e6-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a03e6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a03e6-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a03e6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a03e6-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a03e6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a03e6-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a03e6-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a03e6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a03e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a03e6-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a03e6-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a03e6-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a03e6-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a03e6-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="a03e6-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a03e6-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a03e6-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a03e6-126">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="a03e6-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a03e6-127">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="a03e6-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a03e6-128">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="a03e6-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




