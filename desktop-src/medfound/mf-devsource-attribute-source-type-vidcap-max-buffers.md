---
description: Especifica o número máximo de quadros que a fonte de captura de vídeo armazenará em buffer.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788140"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="6e34b-103">\_Tipo de fonte de atributo DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ \_ atributo Max buffers</span><span class="sxs-lookup"><span data-stu-id="6e34b-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="6e34b-104">Especifica o número máximo de quadros que a fonte de captura de vídeo armazenará em buffer.</span><span class="sxs-lookup"><span data-stu-id="6e34b-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e34b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6e34b-105">Data type</span></span>

<span data-ttu-id="6e34b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6e34b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6e34b-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="6e34b-107">Get/set</span></span>

<span data-ttu-id="6e34b-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6e34b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6e34b-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6e34b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e34b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e34b-110">Remarks</span></span>

<span data-ttu-id="6e34b-111">Por padrão, a fonte de captura de vídeo armazena em buffer um máximo de um quadro por vez.</span><span class="sxs-lookup"><span data-stu-id="6e34b-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="6e34b-112">Você pode aumentar o limite de buffer definindo esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6e34b-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="6e34b-113">A maneira correta de definir esse atributo depende da função usada para criar a origem da mídia:</span><span class="sxs-lookup"><span data-stu-id="6e34b-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="6e34b-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): defina o atributo por meio do parâmetro *pAttributes* da função.</span><span class="sxs-lookup"><span data-stu-id="6e34b-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="6e34b-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): defina o atributo por meio do parâmetro *pAttributes* da função.</span><span class="sxs-lookup"><span data-stu-id="6e34b-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="6e34b-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): defina o atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornado pela função.</span><span class="sxs-lookup"><span data-stu-id="6e34b-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="6e34b-117">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="6e34b-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="6e34b-118">O atributo aplica-se somente a dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e34b-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="6e34b-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6e34b-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e34b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e34b-120">Requirements</span></span>



| <span data-ttu-id="6e34b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e34b-121">Requirement</span></span> | <span data-ttu-id="6e34b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6e34b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e34b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e34b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e34b-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6e34b-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6e34b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e34b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e34b-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6e34b-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6e34b-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e34b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e34b-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e34b-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e34b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e34b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e34b-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e34b-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e34b-131">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="6e34b-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="6e34b-132">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6e34b-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




