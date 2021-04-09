---
description: Especifica a categoria de dispositivo para um dispositivo de captura de vídeo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090689"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="10fec-103">\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ atributo category</span><span class="sxs-lookup"><span data-stu-id="10fec-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="10fec-104">Especifica a categoria de dispositivo para um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10fec-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="10fec-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="10fec-105">Data type</span></span>

<span data-ttu-id="10fec-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="10fec-106">**GUID**</span></span>

<span data-ttu-id="10fec-107">O valor a seguir é definido.</span><span class="sxs-lookup"><span data-stu-id="10fec-107">The following value is defined.</span></span>



| <span data-ttu-id="10fec-108">Valor</span><span class="sxs-lookup"><span data-stu-id="10fec-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="10fec-109">Significado</span><span class="sxs-lookup"><span data-stu-id="10fec-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="10fec-110"><dt>**\_VIDEOINPUTDEVICECATEGORY CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="10fec-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="10fec-111">Dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10fec-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="10fec-112">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="10fec-112">Get/set</span></span>

<span data-ttu-id="10fec-113">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="10fec-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="10fec-114">Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="10fec-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="10fec-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="10fec-115">Remarks</span></span>

<span data-ttu-id="10fec-116">Use esse atributo como entrada para a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) ao enumerar dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10fec-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="10fec-117">Além disso, esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="10fec-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="10fec-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="10fec-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="10fec-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="10fec-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="10fec-120">O atributo aplica-se somente a dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10fec-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="10fec-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="10fec-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10fec-122">Requirements</span></span>



| <span data-ttu-id="10fec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="10fec-123">Requirement</span></span> | <span data-ttu-id="10fec-124">Valor</span><span class="sxs-lookup"><span data-stu-id="10fec-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10fec-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10fec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="10fec-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="10fec-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10fec-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10fec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="10fec-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="10fec-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="10fec-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10fec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fec-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10fec-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fec-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="10fec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fec-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="10fec-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="10fec-133">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="10fec-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="10fec-134">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="10fec-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




