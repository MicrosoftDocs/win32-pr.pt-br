---
description: Especifica o tamanho máximo do pacote, em bytes, de um arquivo ASF (Advanced Systems Format).
ms.assetid: 8dcae150-2363-47ba-b0d3-0bc182574d81
title: Atributo MF_PD_ASF_FILEPROPERTIES_MAX_PACKET_SIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d9c95b7511525570a9e04a33db8128f374f9472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811238"
---
# <a name="mf_pd_asf_fileproperties_max_packet_size-attribute"></a><span data-ttu-id="2b69f-103">\_Atributo de \_ \_ \_ tamanho máximo de \_ pacote \_ de arquivo MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="2b69f-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="2b69f-104">Especifica o tamanho máximo do pacote, em bytes, de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2b69f-104">Specifies the maximum packet size, in bytes, of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b69f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2b69f-105">Data type</span></span>

<span data-ttu-id="2b69f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2b69f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2b69f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b69f-107">Remarks</span></span>

<span data-ttu-id="2b69f-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="2b69f-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2b69f-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="2b69f-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b69f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b69f-110">Requirements</span></span>



| <span data-ttu-id="2b69f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b69f-111">Requirement</span></span> | <span data-ttu-id="2b69f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2b69f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b69f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b69f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2b69f-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b69f-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2b69f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b69f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2b69f-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b69f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2b69f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b69f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b69f-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b69f-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b69f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b69f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b69f-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b69f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b69f-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="2b69f-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2b69f-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="2b69f-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2b69f-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2b69f-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2b69f-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="2b69f-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b69f-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2b69f-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2b69f-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="2b69f-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




