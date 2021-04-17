---
description: Especifica a taxa média de bits, em bits por segundo, de um fluxo em um arquivo de formato de sistema avançado (ASF). Esse atributo corresponde ao objeto de propriedades de taxa de bits de fluxo definido na especificação do ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: Atributo MF_SD_ASF_STREAMBITRATES_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798225"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="fe2d4-104">\_Atributo MF SD \_ ASF \_ STREAMBITRATES taxa de \_ bits</span><span class="sxs-lookup"><span data-stu-id="fe2d4-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="fe2d4-105">Especifica a taxa média de bits, em bits por segundo, de um fluxo em um arquivo de formato de sistema avançado (ASF).</span><span class="sxs-lookup"><span data-stu-id="fe2d4-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="fe2d4-106">Esse atributo corresponde ao objeto de propriedades de taxa de bits de fluxo definido na especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe2d4-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="fe2d4-107">Data type</span></span>

<span data-ttu-id="fe2d4-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fe2d4-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fe2d4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe2d4-109">Remarks</span></span>

<span data-ttu-id="fe2d4-110">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo e o define no descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="fe2d4-111">O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="fe2d4-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="fe2d4-112">O valor do atributo é igual ao campo taxa média de bits no objeto fluxo de propriedades de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="fe2d4-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2d4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe2d4-113">Requirements</span></span>



| <span data-ttu-id="fe2d4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe2d4-114">Requirement</span></span> | <span data-ttu-id="fe2d4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fe2d4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2d4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe2d4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2d4-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe2d4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe2d4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe2d4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2d4-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe2d4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe2d4-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe2d4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe2d4-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe2d4-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe2d4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe2d4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2d4-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe2d4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe2d4-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fe2d4-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fe2d4-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="fe2d4-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fe2d4-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe2d4-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="fe2d4-127">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="fe2d4-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe2d4-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="fe2d4-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




