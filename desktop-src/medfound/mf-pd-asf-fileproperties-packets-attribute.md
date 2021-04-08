---
description: Especifica o número de pacotes na seção de dados de um arquivo ASF (Advanced Systems Format).
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: Atributo MF_PD_ASF_FILEPROPERTIES_PACKETS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920882"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="bddd1-103">\_Atributo de \_ \_ pacotes FileProperties do MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="bddd1-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="bddd1-104">Especifica o número de pacotes na seção de dados de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="bddd1-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="bddd1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bddd1-105">Data type</span></span>

<span data-ttu-id="bddd1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bddd1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bddd1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bddd1-107">Remarks</span></span>

<span data-ttu-id="bddd1-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="bddd1-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="bddd1-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="bddd1-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddd1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bddd1-110">Requirements</span></span>



| <span data-ttu-id="bddd1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bddd1-111">Requirement</span></span> | <span data-ttu-id="bddd1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bddd1-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddd1-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bddd1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bddd1-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bddd1-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bddd1-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bddd1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bddd1-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bddd1-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bddd1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bddd1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bddd1-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="bddd1-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddd1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bddd1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddd1-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bddd1-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bddd1-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bddd1-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bddd1-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="bddd1-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bddd1-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bddd1-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="bddd1-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="bddd1-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="bddd1-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="bddd1-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="bddd1-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="bddd1-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




