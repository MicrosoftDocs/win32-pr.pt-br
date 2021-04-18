---
description: Especifica um tipo de dispositivo, como captura de áudio ou captura de vídeo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807300"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="3ad2c-103">\_Atributo de \_ tipo de fonte de atributo MF DEVSOURCE \_ \_</span><span class="sxs-lookup"><span data-stu-id="3ad2c-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="3ad2c-104">Especifica o tipo de um dispositivo, como captura de áudio ou captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3ad2c-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ad2c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3ad2c-105">Data type</span></span>

<span data-ttu-id="3ad2c-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3ad2c-106">**GUID**</span></span>

<span data-ttu-id="3ad2c-107">Os valores a seguir são definidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="3ad2c-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="3ad2c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad2c-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="3ad2c-109">Significado</span><span class="sxs-lookup"><span data-stu-id="3ad2c-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="3ad2c-110"><dt>**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="3ad2c-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="3ad2c-111">Dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="3ad2c-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="3ad2c-112"><dt>**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="3ad2c-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="3ad2c-113">Dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3ad2c-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="3ad2c-114">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="3ad2c-114">Get/set</span></span>

<span data-ttu-id="3ad2c-115">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="3ad2c-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="3ad2c-116">Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="3ad2c-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad2c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ad2c-117">Remarks</span></span>

<span data-ttu-id="3ad2c-118">Use este atributo como entrada para as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="3ad2c-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="3ad2c-119">**MFCreateDeviceSource**</span><span class="sxs-lookup"><span data-stu-id="3ad2c-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="3ad2c-120">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="3ad2c-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="3ad2c-121">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="3ad2c-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="3ad2c-122">Além disso, esse atributo é definido nos objetos de ativação retornados pela função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="3ad2c-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="3ad2c-123">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3ad2c-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad2c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ad2c-124">Requirements</span></span>



| <span data-ttu-id="3ad2c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ad2c-125">Requirement</span></span> | <span data-ttu-id="3ad2c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad2c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad2c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ad2c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad2c-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3ad2c-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ad2c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ad2c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad2c-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="3ad2c-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3ad2c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ad2c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad2c-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad2c-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad2c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ad2c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad2c-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ad2c-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ad2c-135">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="3ad2c-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="3ad2c-136">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3ad2c-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




