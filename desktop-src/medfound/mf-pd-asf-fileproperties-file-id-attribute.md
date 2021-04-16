---
description: Especifica o identificador de arquivo de um arquivo ASF (Advanced Systems Format).
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: Atributo MF_PD_ASF_FILEPROPERTIES_FILE_ID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751024"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="2ee6e-103">\_Atributo de ID de arquivo MF PD \_ ASF \_ FileProperties \_ \_</span><span class="sxs-lookup"><span data-stu-id="2ee6e-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="2ee6e-104">Especifica o identificador de arquivo de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2ee6e-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2ee6e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2ee6e-105">Data type</span></span>

<span data-ttu-id="2ee6e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2ee6e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee6e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ee6e-107">Remarks</span></span>

<span data-ttu-id="2ee6e-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2ee6e-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="2ee6e-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee6e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee6e-110">Requirements</span></span>



| <span data-ttu-id="2ee6e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee6e-111">Requirement</span></span> | <span data-ttu-id="2ee6e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2ee6e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee6e-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ee6e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee6e-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ee6e-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ee6e-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ee6e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee6e-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ee6e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2ee6e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ee6e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee6e-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee6e-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee6e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ee6e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee6e-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ee6e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ee6e-121">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="2ee6e-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="2ee6e-122">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="2ee6e-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="2ee6e-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2ee6e-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2ee6e-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="2ee6e-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2ee6e-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2ee6e-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2ee6e-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="2ee6e-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




