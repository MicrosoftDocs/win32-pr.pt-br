---
description: Especifica se um arquivo de formato de sistema avançado (ASF) usa codificação de taxa de bits variável (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: Atributo MF_PD_ASF_METADATA_IS_VBR (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811087"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="eec4c-103">Os \_ metadados do MF PD \_ ASF \_ são do \_ \_ atributo VBR</span><span class="sxs-lookup"><span data-stu-id="eec4c-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="eec4c-104">Especifica se um arquivo de formato de sistema avançado (ASF) usa codificação de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="eec4c-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="eec4c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="eec4c-105">Data type</span></span>

<span data-ttu-id="eec4c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eec4c-106">**UINT32**</span></span>

<span data-ttu-id="eec4c-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="eec4c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec4c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="eec4c-108">Remarks</span></span>

<span data-ttu-id="eec4c-109">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="eec4c-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="eec4c-110">Se o valor for **true**, o arquivo foi codificado usando VBR.</span><span class="sxs-lookup"><span data-stu-id="eec4c-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="eec4c-111">Se o valor for **false** ou o atributo não estiver presente, o arquivo não usará a codificação VBR.</span><span class="sxs-lookup"><span data-stu-id="eec4c-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="eec4c-112">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo e o define no descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="eec4c-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="eec4c-113">Esse atributo corresponde ao atributo **IsVBR** no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="eec4c-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eec4c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eec4c-114">Requirements</span></span>



| <span data-ttu-id="eec4c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec4c-115">Requirement</span></span> | <span data-ttu-id="eec4c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="eec4c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eec4c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eec4c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eec4c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eec4c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eec4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eec4c-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eec4c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eec4c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eec4c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eec4c-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec4c-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec4c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="eec4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec4c-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eec4c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eec4c-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="eec4c-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="eec4c-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="eec4c-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="eec4c-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="eec4c-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="eec4c-128">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="eec4c-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="eec4c-129">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="eec4c-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="eec4c-130">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="eec4c-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




