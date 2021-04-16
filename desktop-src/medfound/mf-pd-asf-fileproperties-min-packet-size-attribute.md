---
description: Especifica o tamanho mínimo do pacote, em bytes, para um arquivo ASF (Advanced Systems Format).
ms.assetid: 8c62db36-1332-4565-9fc0-885b9fc148e1
title: Atributo MF_PD_ASF_FILEPROPERTIES_MIN_PACKET_SIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e7b9016184096696ffd74cde6bd51f305778e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751022"
---
# <a name="mf_pd_asf_fileproperties_min_packet_size-attribute"></a><span data-ttu-id="19b99-103">\_Atributo de \_ \_ tamanho de pacote FileProperties \_ min \_ \_ do MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="19b99-103">MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="19b99-104">Especifica o tamanho mínimo do pacote, em bytes, para um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="19b99-104">Specifies the minimum packet size, in bytes, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="19b99-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19b99-105">Data type</span></span>

<span data-ttu-id="19b99-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19b99-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19b99-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="19b99-107">Remarks</span></span>

<span data-ttu-id="19b99-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="19b99-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="19b99-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="19b99-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b99-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19b99-110">Requirements</span></span>



| <span data-ttu-id="19b99-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="19b99-111">Requirement</span></span> | <span data-ttu-id="19b99-112">Valor</span><span class="sxs-lookup"><span data-stu-id="19b99-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b99-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19b99-113">Minimum supported client</span></span><br/> | <span data-ttu-id="19b99-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19b99-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="19b99-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19b99-115">Minimum supported server</span></span><br/> | <span data-ttu-id="19b99-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19b99-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19b99-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19b99-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="19b99-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="19b99-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b99-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="19b99-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b99-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19b99-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19b99-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="19b99-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19b99-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="19b99-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19b99-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="19b99-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="19b99-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="19b99-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="19b99-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="19b99-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="19b99-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="19b99-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




