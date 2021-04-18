---
description: Especifica a quantidade de tempo, em milissegundos, para armazenar em buffer os dados antes de reproduzir um arquivo ASF (Advanced Systems Format).
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: Atributo MF_PD_ASF_FILEPROPERTIES_PREROLL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170517"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="2f27f-103">\_Atributo de \_ preversão do MF PD ASF \_ FileProperties \_</span><span class="sxs-lookup"><span data-stu-id="2f27f-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="2f27f-104">Especifica a quantidade de tempo, em milissegundos, para armazenar em buffer os dados antes de reproduzir um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2f27f-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f27f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2f27f-105">Data type</span></span>

<span data-ttu-id="2f27f-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2f27f-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="2f27f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f27f-107">Remarks</span></span>

<span data-ttu-id="2f27f-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="2f27f-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2f27f-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="2f27f-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f27f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f27f-110">Requirements</span></span>



| <span data-ttu-id="2f27f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f27f-111">Requirement</span></span> | <span data-ttu-id="2f27f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2f27f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f27f-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f27f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2f27f-114">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f27f-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2f27f-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f27f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2f27f-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f27f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f27f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f27f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f27f-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f27f-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f27f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f27f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f27f-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f27f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f27f-121">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="2f27f-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="2f27f-122">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="2f27f-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="2f27f-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2f27f-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2f27f-124">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="2f27f-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f27f-125">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="2f27f-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2f27f-126">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="2f27f-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




