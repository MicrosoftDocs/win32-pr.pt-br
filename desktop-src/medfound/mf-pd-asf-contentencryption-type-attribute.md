---
description: Especifica o tipo de mecanismo de proteção usado em um arquivo ASF (Advanced Systems Format).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_TYPE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827080"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="26436-103">\_Atributo de \_ \_ tipo de CONTENTENCRYPTION MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="26436-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="26436-104">Especifica o tipo de mecanismo de proteção usado em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="26436-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="26436-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="26436-105">Data type</span></span>

<span data-ttu-id="26436-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="26436-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="26436-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="26436-107">Remarks</span></span>

<span data-ttu-id="26436-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="26436-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="26436-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera o campo de tipo de proteção, converte-o em uma cadeia de caracteres largo e, em seguida, popula uma matriz terminada em nulo de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="26436-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="26436-110">Se presente, o valor deve ser "DRM".</span><span class="sxs-lookup"><span data-stu-id="26436-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="26436-111">O tamanho da matriz é igual ao campo de tamanho do campo de tipo de proteção do cabeçalho de criptografia de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="26436-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="26436-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26436-112">Requirements</span></span>



| <span data-ttu-id="26436-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="26436-113">Requirement</span></span> | <span data-ttu-id="26436-114">Valor</span><span class="sxs-lookup"><span data-stu-id="26436-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26436-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26436-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26436-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26436-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26436-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26436-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26436-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26436-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="26436-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26436-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="26436-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="26436-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26436-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="26436-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26436-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26436-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="26436-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="26436-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="26436-124">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="26436-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="26436-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="26436-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="26436-126">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="26436-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="26436-127">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="26436-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="26436-128">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="26436-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




