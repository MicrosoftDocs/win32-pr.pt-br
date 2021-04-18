---
description: Especifica o tamanho máximo do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: Atributo MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce31dfacd1d53cadcc38b37e1cb755c330a7882f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785018"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a><span data-ttu-id="a835d-103">\_ \_ \_ \_ Atributo BUFFERSIZE de EXTSTRMPROP do MF SD ASF \_</span><span class="sxs-lookup"><span data-stu-id="a835d-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="a835d-104">Especifica o tamanho máximo do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a835d-104">Specifies the maximum buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a835d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a835d-105">Data type</span></span>

<span data-ttu-id="a835d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a835d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a835d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a835d-107">Remarks</span></span>

<span data-ttu-id="a835d-108">Esse atributo se aplica a descritores de fluxo para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="a835d-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="a835d-109">Ele corresponde ao campo tamanho de buffer alternativo no objeto Propriedades de fluxo estendido.</span><span class="sxs-lookup"><span data-stu-id="a835d-109">It corresponds to the Alternate Buffer Size field in the Extended Stream Properties object.</span></span> <span data-ttu-id="a835d-110">Para obter mais informações, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="a835d-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="a835d-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="a835d-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="a835d-112">O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="a835d-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="a835d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a835d-113">Requirements</span></span>



| <span data-ttu-id="a835d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a835d-114">Requirement</span></span> | <span data-ttu-id="a835d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a835d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a835d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a835d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a835d-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a835d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a835d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a835d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a835d-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a835d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a835d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a835d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a835d-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a835d-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a835d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a835d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a835d-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a835d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a835d-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a835d-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a835d-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="a835d-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a835d-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a835d-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="a835d-127">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="a835d-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a835d-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="a835d-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




