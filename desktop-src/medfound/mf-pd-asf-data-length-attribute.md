---
description: Especifica o tamanho, em bytes, da seção de dados de um arquivo de formato de sistema avançado (ASF).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: Atributo MF_PD_ASF_DATA_LENGTH (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755267"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="63771-103">Atributo de comprimento de dados do MF \_ PD \_ ASF \_ \_</span><span class="sxs-lookup"><span data-stu-id="63771-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="63771-104">Especifica o tamanho, em bytes, da seção de dados de um arquivo de formato de sistema avançado (ASF).</span><span class="sxs-lookup"><span data-stu-id="63771-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="63771-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="63771-105">Data type</span></span>

<span data-ttu-id="63771-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="63771-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="63771-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="63771-107">Remarks</span></span>

<span data-ttu-id="63771-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="63771-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="63771-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="63771-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="63771-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63771-110">Requirements</span></span>



| <span data-ttu-id="63771-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="63771-111">Requirement</span></span> | <span data-ttu-id="63771-112">Valor</span><span class="sxs-lookup"><span data-stu-id="63771-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="63771-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63771-113">Minimum supported client</span></span><br/> | <span data-ttu-id="63771-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63771-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63771-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63771-115">Minimum supported server</span></span><br/> | <span data-ttu-id="63771-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63771-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63771-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63771-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="63771-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="63771-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63771-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="63771-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63771-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63771-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63771-121">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="63771-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="63771-122">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="63771-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="63771-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="63771-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="63771-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="63771-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="63771-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="63771-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




