---
description: Especifica o tamanho médio do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: Atributo MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828922"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="62b2d-103">Atributo de BUFFERSIZE do EXTSTRMPROP do MF \_ SD \_ ASF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="62b2d-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="62b2d-104">Especifica o tamanho médio do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="62b2d-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="62b2d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="62b2d-105">Data type</span></span>

<span data-ttu-id="62b2d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="62b2d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62b2d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="62b2d-107">Remarks</span></span>

<span data-ttu-id="62b2d-108">Esse atributo se aplica a descritores de fluxo para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="62b2d-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="62b2d-109">Ele corresponde ao campo tamanho do buffer no objeto Propriedades do fluxo estendido e define o tamanho do Bucket usado no modelo "Bucket de vazamentos".</span><span class="sxs-lookup"><span data-stu-id="62b2d-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="62b2d-110">Para obter mais informações, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="62b2d-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="62b2d-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="62b2d-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="62b2d-112">O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="62b2d-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="62b2d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62b2d-113">Requirements</span></span>



| <span data-ttu-id="62b2d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62b2d-114">Requirement</span></span> | <span data-ttu-id="62b2d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="62b2d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b2d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62b2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62b2d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62b2d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="62b2d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62b2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62b2d-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62b2d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="62b2d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62b2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62b2d-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="62b2d-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b2d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="62b2d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b2d-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62b2d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62b2d-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="62b2d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="62b2d-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="62b2d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="62b2d-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="62b2d-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="62b2d-127">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="62b2d-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="62b2d-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="62b2d-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




