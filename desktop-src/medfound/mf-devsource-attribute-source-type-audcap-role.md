---
description: Especifica a função de dispositivo para um dispositivo de captura de áudio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010720"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a><span data-ttu-id="de35d-103">\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP atributo de \_ função</span><span class="sxs-lookup"><span data-stu-id="de35d-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ROLE attribute</span></span>

<span data-ttu-id="de35d-104">Especifica a função de dispositivo para um dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="de35d-104">Specifies the device role for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="de35d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="de35d-105">Data type</span></span>

<span data-ttu-id="de35d-106">**ERole** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="de35d-106">**ERole** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="de35d-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="de35d-107">Get/set</span></span>

<span data-ttu-id="de35d-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="de35d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="de35d-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="de35d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="de35d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="de35d-110">Remarks</span></span>

<span data-ttu-id="de35d-111">O tipo de enumeração **eRole** está documentado na documentação da API de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="de35d-111">The **eRole** enumeration type is documented in the Core Audio API documentation.</span></span>

<span data-ttu-id="de35d-112">O valor do atributo especifica uma função de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de35d-112">The value of the attribute specifies a device role.</span></span> <span data-ttu-id="de35d-113">Esse atributo é usado com as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="de35d-113">This attribute is used with the following functions.</span></span>

<span data-ttu-id="de35d-114">Esse atributo pode ser usado como entrada para as funções [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="de35d-114">This attribute can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="de35d-115">Se o atributo for especificado, a função criará uma fonte de mídia que usa o dispositivo de captura de áudio padrão para a função de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="de35d-115">If the attribute is specified, the function creates a media source that uses the default audio capture device for the specified device role.</span></span>

<span data-ttu-id="de35d-116">Esse atributo também pode ser usado como entrada para a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="de35d-116">This attribute can also be used as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="de35d-117">Se o atributo for especificado, a enumeração será restrita à função de dispositivo especificada.</span><span class="sxs-lookup"><span data-stu-id="de35d-117">If the attribute is specified, the enumeration is restricted to the specified device role.</span></span> <span data-ttu-id="de35d-118">Além disso, cada objeto de ativação retornado pela função **MFEnumDeviceSources** contém esse atributo.</span><span class="sxs-lookup"><span data-stu-id="de35d-118">In addition, each activation object returned by the **MFEnumDeviceSources** function contains this attribute.</span></span> <span data-ttu-id="de35d-119">O atributo é então usado internamente pelo objeto de ativação quando cria a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="de35d-119">The attribute is then used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="de35d-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="de35d-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de35d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de35d-121">Requirements</span></span>



| <span data-ttu-id="de35d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="de35d-122">Requirement</span></span> | <span data-ttu-id="de35d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="de35d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de35d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de35d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="de35d-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="de35d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de35d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de35d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="de35d-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="de35d-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="de35d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de35d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="de35d-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de35d-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de35d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="de35d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de35d-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de35d-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="de35d-132">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="de35d-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="de35d-133">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="de35d-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




