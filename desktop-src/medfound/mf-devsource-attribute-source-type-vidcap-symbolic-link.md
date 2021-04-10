---
description: Contém o link simbólico para um driver de captura de vídeo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091157"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a><span data-ttu-id="d0fdd-103">\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP atributo de \_ \_ link simbólico</span><span class="sxs-lookup"><span data-stu-id="d0fdd-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute</span></span>

<span data-ttu-id="d0fdd-104">Contém o link simbólico para um driver de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-104">Contains the symbolic link for a video capture driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0fdd-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d0fdd-105">Data type</span></span>

<span data-ttu-id="d0fdd-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d0fdd-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="d0fdd-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="d0fdd-107">Get/set</span></span>

<span data-ttu-id="d0fdd-108">Para obter esse atributo, chame [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="d0fdd-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="d0fdd-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="d0fdd-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0fdd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0fdd-110">Remarks</span></span>

<span data-ttu-id="d0fdd-111">Use esse atributo como entrada para a função [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="d0fdd-111">Use this attribute as input to the [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="d0fdd-112">Além disso, esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="d0fdd-112">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="d0fdd-113">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="d0fdd-113">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="d0fdd-114">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="d0fdd-114">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="d0fdd-115">O link simbólico deve ser considerado uma cadeia de caracteres opaca.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-115">The symbolic link should be considered an opaque string.</span></span> <span data-ttu-id="d0fdd-116">O nome de exibição legível por humanos de um dispositivo está contido no atributo de [ \_ \_ \_ \_ nome amigável do atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .</span><span class="sxs-lookup"><span data-stu-id="d0fdd-116">The human-readable display name for a device is contained in the [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute.</span></span>

<span data-ttu-id="d0fdd-117">O atributo de DEVSOURCE MF do \_ \_ tipo de \_ origem \_ \_ VIDCAP \_ \_ de link simbólico pode ser passado como o valor do argumento DevicePath da função [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .</span><span class="sxs-lookup"><span data-stu-id="d0fdd-117">The MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK attribute can be passed in as the value of the DevicePath argument of the [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) function.</span></span>

<span data-ttu-id="d0fdd-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d0fdd-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0fdd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0fdd-119">Requirements</span></span>



| <span data-ttu-id="d0fdd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0fdd-120">Requirement</span></span> | <span data-ttu-id="d0fdd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d0fdd-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fdd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d0fdd-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0fdd-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d0fdd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0fdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d0fdd-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d0fdd-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d0fdd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0fdd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0fdd-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fdd-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fdd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0fdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fdd-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0fdd-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0fdd-130">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="d0fdd-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="d0fdd-131">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d0fdd-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
