---
description: Especifica se uma fonte de captura de vídeo é um dispositivo de hardware ou um dispositivo de software.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748680"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="d0332-103">\_Tipo de origem de atributo MF DEVSOURCE, atributo de \_ \_ \_ \_ \_ origem HW VIDCAP \_</span><span class="sxs-lookup"><span data-stu-id="d0332-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="d0332-104">Especifica se uma fonte de captura de vídeo é um dispositivo de hardware ou um dispositivo de software.</span><span class="sxs-lookup"><span data-stu-id="d0332-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0332-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d0332-105">Data type</span></span>

<span data-ttu-id="d0332-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d0332-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d0332-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="d0332-107">Get/set</span></span>

<span data-ttu-id="d0332-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d0332-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d0332-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d0332-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0332-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0332-110">Remarks</span></span>

<span data-ttu-id="d0332-111">Se o valor for **true**, a origem da captura será um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="d0332-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="d0332-112">Se o valor for **false**, ele será um dispositivo de software.</span><span class="sxs-lookup"><span data-stu-id="d0332-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="d0332-113">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="d0332-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="d0332-114">Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="d0332-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="d0332-115">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="d0332-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="d0332-116">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="d0332-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="d0332-117">O atributo aplica-se somente a dispositivos de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0332-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="d0332-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d0332-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0332-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0332-119">Requirements</span></span>



| <span data-ttu-id="d0332-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0332-120">Requirement</span></span> | <span data-ttu-id="d0332-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d0332-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0332-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0332-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d0332-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0332-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d0332-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0332-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d0332-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d0332-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d0332-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0332-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0332-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0332-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0332-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0332-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0332-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0332-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0332-130">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="d0332-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="d0332-131">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d0332-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




