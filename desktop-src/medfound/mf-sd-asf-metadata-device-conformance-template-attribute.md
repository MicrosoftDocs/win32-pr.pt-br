---
description: Especifica o modelo de conformidade do dispositivo para um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: Atributo MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793648"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="dfaed-103">\_Atributo de \_ \_ modelo de \_ conformidade do dispositivo de metadados do \_ MF SD \_</span><span class="sxs-lookup"><span data-stu-id="dfaed-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="dfaed-104">Especifica o modelo de conformidade do dispositivo para um fluxo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="dfaed-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="dfaed-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dfaed-105">Data type</span></span>

<span data-ttu-id="dfaed-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="dfaed-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="dfaed-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfaed-107">Remarks</span></span>

<span data-ttu-id="dfaed-108">Esse atributo se aplica a descritores de fluxo para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="dfaed-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="dfaed-109">Para obter mais informações sobre modelos de conformidade do dispositivo, consulte o tópico "parâmetros de modelo de conformidade do dispositivo" no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="dfaed-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="dfaed-110">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.</span><span class="sxs-lookup"><span data-stu-id="dfaed-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfaed-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfaed-111">Requirements</span></span>



| <span data-ttu-id="dfaed-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfaed-112">Requirement</span></span> | <span data-ttu-id="dfaed-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dfaed-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaed-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaed-114">Minimum supported client</span></span><br/> | <span data-ttu-id="dfaed-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfaed-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dfaed-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaed-116">Minimum supported server</span></span><br/> | <span data-ttu-id="dfaed-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfaed-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dfaed-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfaed-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfaed-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfaed-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfaed-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfaed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfaed-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dfaed-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dfaed-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="dfaed-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="dfaed-123">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="dfaed-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="dfaed-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="dfaed-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="dfaed-125">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="dfaed-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="dfaed-126">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="dfaed-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




