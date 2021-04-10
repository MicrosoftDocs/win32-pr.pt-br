---
description: Especifica o identificador de chave para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de ID de chave do cabeçalho de criptografia de conteúdo, definido na especificação de ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_KEYID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090298"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a><span data-ttu-id="4ba5a-104">\_ \_ \_ Atributo keyid PD ASF CONTENTENCRYPTION \_ do MF</span><span class="sxs-lookup"><span data-stu-id="4ba5a-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_KEYID attribute</span></span>

<span data-ttu-id="4ba5a-105">Especifica o identificador de chave para um arquivo ASF (Encrypt Systems Format) criptografado.</span><span class="sxs-lookup"><span data-stu-id="4ba5a-105">Specifies the key identifier for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="4ba5a-106">Esse atributo corresponde ao campo de ID de chave do cabeçalho de criptografia de conteúdo, definido na especificação de ASF.</span><span class="sxs-lookup"><span data-stu-id="4ba5a-106">This attribute corresponds to the Key ID field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ba5a-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4ba5a-107">Data type</span></span>

<span data-ttu-id="4ba5a-108">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="4ba5a-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4ba5a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ba5a-109">Remarks</span></span>

<span data-ttu-id="4ba5a-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="4ba5a-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="4ba5a-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera o campo ID da chave, converte-o em uma cadeia de caracteres largos e, em seguida, popula uma matriz terminada em nulo de **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="4ba5a-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Key ID field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="4ba5a-112">O tamanho da matriz é igual ao campo de comprimento da ID de chave do cabeçalho de criptografia de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4ba5a-112">The size of the array equals the Key ID Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba5a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ba5a-113">Requirements</span></span>



| <span data-ttu-id="4ba5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ba5a-114">Requirement</span></span> | <span data-ttu-id="4ba5a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4ba5a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba5a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ba5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba5a-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ba5a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ba5a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ba5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba5a-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ba5a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4ba5a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ba5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba5a-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba5a-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba5a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ba5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba5a-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ba5a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ba5a-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="4ba5a-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4ba5a-125">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="4ba5a-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4ba5a-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4ba5a-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4ba5a-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="4ba5a-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ba5a-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="4ba5a-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="4ba5a-129">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="4ba5a-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




