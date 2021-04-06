---
description: Especifica a taxa máxima de bits instantâneas, em bits por segundo, para um arquivo de formato de sistema avançado (ASF).
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: Atributo MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828317"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="e7ccf-103">\_Atributo MF PD \_ ASF \_ FileProperties \_ Max taxa de \_ bits</span><span class="sxs-lookup"><span data-stu-id="e7ccf-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="e7ccf-104">Especifica a taxa máxima de bits instantâneas, em bits por segundo, para um arquivo de formato de sistema avançado (ASF).</span><span class="sxs-lookup"><span data-stu-id="e7ccf-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="e7ccf-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e7ccf-105">Data type</span></span>

<span data-ttu-id="e7ccf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ccf-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7ccf-107">Remarks</span></span>

<span data-ttu-id="e7ccf-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="e7ccf-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ccf-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ccf-110">Requirements</span></span>



| <span data-ttu-id="e7ccf-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ccf-111">Requirement</span></span> | <span data-ttu-id="e7ccf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e7ccf-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ccf-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ccf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ccf-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7ccf-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7ccf-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ccf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ccf-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7ccf-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e7ccf-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7ccf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ccf-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ccf-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ccf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7ccf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ccf-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7ccf-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e7ccf-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e7ccf-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="e7ccf-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="e7ccf-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="e7ccf-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="e7ccf-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




