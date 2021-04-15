---
description: Especifica a taxa média de bits de dados, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 3a0b39ab-e9a9-49df-a321-a88559aec16f
title: Atributo MF_SD_ASF_EXTSTRMPROP_AVG_DATA_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18789fbd18f063c59de712cf1b1b6bdac1c38a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747469"
---
# <a name="mf_sd_asf_extstrmprop_avg_data_bitrate-attribute"></a><span data-ttu-id="64df3-103">\_Atributo de \_ taxa \_ de \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP</span><span class="sxs-lookup"><span data-stu-id="64df3-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE attribute</span></span>

<span data-ttu-id="64df3-104">Especifica a taxa média de bits de dados, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="64df3-104">Specifies the average data bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="64df3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="64df3-105">Data type</span></span>

<span data-ttu-id="64df3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="64df3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="64df3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="64df3-107">Remarks</span></span>

<span data-ttu-id="64df3-108">Esse atributo se aplica a descritores de fluxo para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="64df3-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="64df3-109">Ele corresponde ao campo de taxa de bits de dados no objeto de propriedades de fluxo estendido e define a taxa de vazamento usada no modelo "Bucket de vazamentos".</span><span class="sxs-lookup"><span data-stu-id="64df3-109">It corresponds to the Data Bit Rate field in the Extended Stream Properties object, and defines the leak rate used in the "leaky bucket" model.</span></span> <span data-ttu-id="64df3-110">Para obter mais informações, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="64df3-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="64df3-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="64df3-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="64df3-112">O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="64df3-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="64df3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64df3-113">Requirements</span></span>



| <span data-ttu-id="64df3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="64df3-114">Requirement</span></span> | <span data-ttu-id="64df3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="64df3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64df3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64df3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64df3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64df3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="64df3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64df3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64df3-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64df3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64df3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64df3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64df3-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="64df3-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64df3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="64df3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64df3-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64df3-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="64df3-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="64df3-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="64df3-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="64df3-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="64df3-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="64df3-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="64df3-127">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="64df3-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="64df3-128">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="64df3-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




