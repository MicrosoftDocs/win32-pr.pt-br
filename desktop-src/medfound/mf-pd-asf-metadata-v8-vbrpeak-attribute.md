---
description: Especifica a taxa de bits momentânea mais alta em um arquivo de formato de sistema avançado (VBR) de taxa de bits variável.
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: Atributo MF_PD_ASF_METADATA_V8_VBRPEAK (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506026"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="19e8b-103">\_Atributo MF PD \_ ASF \_ Metadata \_ V8 \_ VBRPEAK</span><span class="sxs-lookup"><span data-stu-id="19e8b-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="19e8b-104">Especifica a taxa de bits momentânea mais alta em um arquivo de formato de sistema avançado (VBR) de taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="19e8b-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="19e8b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19e8b-105">Data type</span></span>

<span data-ttu-id="19e8b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19e8b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19e8b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="19e8b-107">Remarks</span></span>

<span data-ttu-id="19e8b-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="19e8b-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="19e8b-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo.</span><span class="sxs-lookup"><span data-stu-id="19e8b-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="19e8b-110">Esse atributo aplica-se somente a arquivos criados pela versão 8 do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="19e8b-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="19e8b-111">Ele corresponde ao atributo **VBRPeak** no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="19e8b-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19e8b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19e8b-112">Requirements</span></span>



| <span data-ttu-id="19e8b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e8b-113">Requirement</span></span> | <span data-ttu-id="19e8b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="19e8b-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e8b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19e8b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="19e8b-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19e8b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="19e8b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19e8b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="19e8b-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19e8b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19e8b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19e8b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e8b-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="19e8b-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e8b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="19e8b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e8b-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19e8b-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19e8b-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19e8b-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19e8b-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="19e8b-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19e8b-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="19e8b-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="19e8b-126">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="19e8b-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="19e8b-127">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="19e8b-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="19e8b-128">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="19e8b-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




