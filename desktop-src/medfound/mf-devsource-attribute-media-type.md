---
description: Especifica o formato de saída de um dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Atributo MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759845"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a><span data-ttu-id="5dbeb-103">\_Atributo de \_ tipo de mídia de atributo MF DEVSOURCE \_ \_</span><span class="sxs-lookup"><span data-stu-id="5dbeb-103">MF\_DEVSOURCE\_ATTRIBUTE\_MEDIA\_TYPE attribute</span></span>

<span data-ttu-id="5dbeb-104">Especifica o formato de saída de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-104">Specifies the output format of a device.</span></span>

## <a name="data-type"></a><span data-ttu-id="5dbeb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5dbeb-105">Data type</span></span>

<span data-ttu-id="5dbeb-106">**[**MFT \_ \_ \_ Informações de tipo de registro**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** armazenadas como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-106">**[**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="5dbeb-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5dbeb-107">Get/set</span></span>

<span data-ttu-id="5dbeb-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="5dbeb-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="5dbeb-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="5dbeb-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="5dbeb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dbeb-110">Remarks</span></span>

<span data-ttu-id="5dbeb-111">Este atributo contém um par de GUIDs: um tipo principal e um subtipo.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-111">This attribute contains a pair of GUIDs: a major type and a subtype.</span></span> <span data-ttu-id="5dbeb-112">Essas GUIDs descrevem o formato de saída padrão do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-112">These GUIDs describe the default output format of the device.</span></span> <span data-ttu-id="5dbeb-113">O dispositivo pode dar suporte a formatos de saída adicionais.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-113">The device might support additional output formats.</span></span>

<span data-ttu-id="5dbeb-114">Por exemplo, se um dispositivo de captura de vídeo produzir vídeo RGB-32, o valor desse atributo será `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .</span><span class="sxs-lookup"><span data-stu-id="5dbeb-114">For example, if a video capture device outputs RGB-32 video, the value of this attribute is `{ MFMediaType_Video, MFVideoFormat_RGB32 }`.</span></span>

<span data-ttu-id="5dbeb-115">Esse atributo é uma dica para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-115">This attribute is a hint to the application.</span></span> <span data-ttu-id="5dbeb-116">Para obter o formato de saída exato, crie a origem da mídia para o dispositivo e obtenha o descritor de apresentação da origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-116">To get the exact output format, create the media source for the device and get the media source's presentation descriptor.</span></span>

<span data-ttu-id="5dbeb-117">Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="5dbeb-117">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="5dbeb-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="5dbeb-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="5dbeb-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="5dbeb-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5dbeb-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dbeb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dbeb-121">Requirements</span></span>



| <span data-ttu-id="5dbeb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dbeb-122">Requirement</span></span> | <span data-ttu-id="5dbeb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5dbeb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbeb-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dbeb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5dbeb-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5dbeb-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dbeb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5dbeb-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5dbeb-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5dbeb-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dbeb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dbeb-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dbeb-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dbeb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dbeb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbeb-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5dbeb-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-132">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-132">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="5dbeb-133">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5dbeb-133">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




