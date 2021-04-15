---
description: Contém dados secretos para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de dados secreto do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501638"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="b3169-104">Atributo de dados de segredo do MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_</span><span class="sxs-lookup"><span data-stu-id="b3169-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="b3169-105">Contém dados secretos para um arquivo ASF (Encrypt Systems Format) criptografado.</span><span class="sxs-lookup"><span data-stu-id="b3169-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b3169-106">Esse atributo corresponde ao campo de dados secreto do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="b3169-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3169-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b3169-107">Data type</span></span>

<span data-ttu-id="b3169-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="b3169-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="b3169-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3169-109">Remarks</span></span>

<span data-ttu-id="b3169-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="b3169-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b3169-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) popula uma matriz de bytes com o campo de dados secreto.</span><span class="sxs-lookup"><span data-stu-id="b3169-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="b3169-112">O tamanho da matriz é igual ao campo de comprimento de dados secreto do cabeçalho de criptografia de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b3169-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3169-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3169-113">Requirements</span></span>



| <span data-ttu-id="b3169-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3169-114">Requirement</span></span> | <span data-ttu-id="b3169-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b3169-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3169-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3169-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3169-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3169-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b3169-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3169-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3169-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3169-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3169-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3169-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3169-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3169-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3169-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3169-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3169-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3169-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3169-124">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="b3169-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="b3169-125">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="b3169-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="b3169-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b3169-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b3169-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="b3169-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3169-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="b3169-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b3169-129">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="b3169-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




