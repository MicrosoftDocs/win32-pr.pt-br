---
description: Contém dados de criptografia para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de criptografia de conteúdo estendido no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Atributo MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296561"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="a9aaa-104">\_Atributo de dados de criptografia MF PD \_ ASF \_ CONTENTENCRYPTIONEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="a9aaa-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="a9aaa-105">Contém dados de criptografia para um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a9aaa-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="a9aaa-106">Esse atributo corresponde ao objeto de criptografia de conteúdo estendido no cabeçalho ASF, definido na especificação ASF.</span><span class="sxs-lookup"><span data-stu-id="a9aaa-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="a9aaa-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a9aaa-107">Data type</span></span>

<span data-ttu-id="a9aaa-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="a9aaa-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="a9aaa-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9aaa-109">Remarks</span></span>

<span data-ttu-id="a9aaa-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="a9aaa-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="a9aaa-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo do cabeçalho de objeto de criptografia de conteúdo estendido.</span><span class="sxs-lookup"><span data-stu-id="a9aaa-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="a9aaa-112">O tamanho do blob é igual ao campo tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="a9aaa-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="a9aaa-113">A matriz de bytes contida no blob é igual ao campo de dados no objeto de criptografia de conteúdo estendido do cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="a9aaa-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9aaa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9aaa-114">Requirements</span></span>



| <span data-ttu-id="a9aaa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9aaa-115">Requirement</span></span> | <span data-ttu-id="a9aaa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a9aaa-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9aaa-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9aaa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9aaa-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9aaa-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a9aaa-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9aaa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9aaa-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9aaa-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9aaa-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9aaa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9aaa-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9aaa-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9aaa-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9aaa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9aaa-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9aaa-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9aaa-125">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="a9aaa-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="a9aaa-126">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="a9aaa-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="a9aaa-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a9aaa-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a9aaa-128">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="a9aaa-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9aaa-129">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="a9aaa-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="a9aaa-130">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="a9aaa-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




