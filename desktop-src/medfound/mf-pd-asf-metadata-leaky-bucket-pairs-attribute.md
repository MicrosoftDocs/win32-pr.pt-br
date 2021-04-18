---
description: Especifica uma lista de taxas de bits e janelas de buffer correspondentes para um arquivo de formato ASF (taxa de bits variável).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Atributo MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7426d15a806a8c61c9a2ea1fdfb0565372c5f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802095"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a><span data-ttu-id="3194c-103">\_Atributo de \_ \_ pares de \_ buckets de vazamento de metadados \_ do MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="3194c-103">MF\_PD\_ASF\_METADATA\_LEAKY\_BUCKET\_PAIRS attribute</span></span>

<span data-ttu-id="3194c-104">Especifica uma lista de taxas de bits e janelas de buffer correspondentes para um arquivo de formato ASF (taxa de bits variável).</span><span class="sxs-lookup"><span data-stu-id="3194c-104">Specifies a list of bit rates and corresponding buffer windows for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="3194c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3194c-105">Data type</span></span>

<span data-ttu-id="3194c-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="3194c-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="3194c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3194c-107">Remarks</span></span>

<span data-ttu-id="3194c-108">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="3194c-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="3194c-109">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo que se aplica ao descritor de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="3194c-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

<span data-ttu-id="3194c-110">O valor do atributo tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="3194c-110">The value of the attribute has the following format:</span></span>

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="3194c-111">A estrutura do **\_ \_ \_ par de buckets de vazamento do WM** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3194c-111">The **WM\_LEAKY\_BUCKET\_PAIR** structure is defined as follows:</span></span>

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

<span data-ttu-id="3194c-112">Para cada taxa de bits, o membro **msBufferWindow** indica a quantidade de conteúdo armazenada em buffer antes do início da reprodução, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3194c-112">For each bit rate, the **msBufferWindow** member indicates how much content is buffered before playback begins, in milliseconds.</span></span> <span data-ttu-id="3194c-113">O tamanho do buffer em bytes é igual a **msBufferWinow** x **dwBitrate** /8000.</span><span class="sxs-lookup"><span data-stu-id="3194c-113">The size of the buffer in bytes equals **msBufferWinow** x **dwBitrate** / 8000.</span></span>

> [!Note]  
> <span data-ttu-id="3194c-114">Esse atributo corresponde ao atributo **ASFLeakyBucketPairs** no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="3194c-114">This attribute corresponds to the **ASFLeakyBucketPairs** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3194c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3194c-115">Requirements</span></span>



| <span data-ttu-id="3194c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3194c-116">Requirement</span></span> | <span data-ttu-id="3194c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3194c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3194c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3194c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3194c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3194c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3194c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3194c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3194c-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3194c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3194c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3194c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3194c-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3194c-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3194c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3194c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3194c-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3194c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3194c-126">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="3194c-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="3194c-127">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="3194c-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="3194c-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3194c-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3194c-129">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="3194c-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3194c-130">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="3194c-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="3194c-131">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="3194c-131">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




