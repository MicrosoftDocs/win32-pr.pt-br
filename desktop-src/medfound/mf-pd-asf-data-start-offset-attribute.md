---
description: Especifica o deslocamento, em bytes, desde o início de um arquivo ASF (Advanced Systems Format) até o início do primeiro pacote de dados.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: Atributo MF_PD_ASF_DATA_START_OFFSET (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829600"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="62c38-103">Atributo de deslocamento de início de dados do MF \_ PD \_ ASF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="62c38-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="62c38-104">Especifica o deslocamento, em bytes, desde o início de um arquivo ASF (Advanced Systems Format) até o início do primeiro pacote de dados.</span><span class="sxs-lookup"><span data-stu-id="62c38-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="62c38-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="62c38-105">Data type</span></span>

<span data-ttu-id="62c38-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="62c38-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="62c38-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="62c38-107">Remarks</span></span>

<span data-ttu-id="62c38-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="62c38-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="62c38-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="62c38-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c38-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c38-110">Requirements</span></span>



| <span data-ttu-id="62c38-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c38-111">Requirement</span></span> | <span data-ttu-id="62c38-112">Valor</span><span class="sxs-lookup"><span data-stu-id="62c38-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c38-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c38-113">Minimum supported client</span></span><br/> | <span data-ttu-id="62c38-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62c38-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="62c38-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62c38-115">Minimum supported server</span></span><br/> | <span data-ttu-id="62c38-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62c38-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="62c38-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62c38-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c38-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c38-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c38-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="62c38-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c38-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62c38-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62c38-121">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="62c38-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="62c38-122">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="62c38-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="62c38-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="62c38-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="62c38-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="62c38-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="62c38-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="62c38-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




