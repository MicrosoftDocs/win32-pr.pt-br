---
description: Especifica a data e a hora em que um arquivo ASF (Advanced Systems Format) foi criado.
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Atributo MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920883"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="083d1-103">Atributo de tempo de criação do MF \_ PD \_ ASF \_ FileProperties \_ \_</span><span class="sxs-lookup"><span data-stu-id="083d1-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="083d1-104">Especifica a data e a hora em que um arquivo ASF (Advanced Systems Format) foi criado.</span><span class="sxs-lookup"><span data-stu-id="083d1-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="083d1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="083d1-105">Data type</span></span>

<span data-ttu-id="083d1-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="083d1-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="083d1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="083d1-107">Remarks</span></span>

<span data-ttu-id="083d1-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="083d1-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="083d1-109">O valor do atributo é uma estrutura **FILETIME** , que é documentada na SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="083d1-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="083d1-110">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="083d1-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="083d1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="083d1-111">Requirements</span></span>



| <span data-ttu-id="083d1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="083d1-112">Requirement</span></span> | <span data-ttu-id="083d1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="083d1-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="083d1-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="083d1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="083d1-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="083d1-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="083d1-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="083d1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="083d1-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="083d1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="083d1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="083d1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="083d1-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="083d1-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="083d1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="083d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="083d1-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="083d1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="083d1-122">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="083d1-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="083d1-123">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="083d1-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="083d1-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="083d1-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="083d1-125">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="083d1-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="083d1-126">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="083d1-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="083d1-127">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="083d1-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




