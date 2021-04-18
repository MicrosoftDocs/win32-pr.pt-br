---
description: Especifica a ID do ponto de extremidade para um dispositivo de captura de áudio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781365"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a><span data-ttu-id="0c1a9-103">\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ atributo ID do ponto de extremidade \_</span><span class="sxs-lookup"><span data-stu-id="0c1a9-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="0c1a9-104">Especifica a ID do ponto de extremidade para um dispositivo de captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-104">Specifies the endpoint ID for an audio capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c1a9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0c1a9-105">Data type</span></span>

<span data-ttu-id="0c1a9-106">**WCHAR\***</span><span class="sxs-lookup"><span data-stu-id="0c1a9-106">**WCHAR\***</span></span>

## <a name="getset"></a><span data-ttu-id="0c1a9-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0c1a9-107">Get/set</span></span>

<span data-ttu-id="0c1a9-108">Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="0c1a9-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="0c1a9-109">Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="0c1a9-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c1a9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c1a9-110">Remarks</span></span>

<span data-ttu-id="0c1a9-111">O valor do atributo é uma ID de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-111">The value of the attribute is an endpoint ID.</span></span> <span data-ttu-id="0c1a9-112">Esse atributo é usado com as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="0c1a9-112">This attribute is used with the following functions:</span></span>

-   <span data-ttu-id="0c1a9-113">Ele pode ser usado como entrada para as funções [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="0c1a9-113">It can be used as input to the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) and [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) functions.</span></span> <span data-ttu-id="0c1a9-114">Nesse contexto, o atributo especifica o dispositivo de captura de áudio para a função.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-114">In this context, the attribute specifies the audio capture device for the function.</span></span> <span data-ttu-id="0c1a9-115">Você pode obter a ID do ponto de extremidade para um determinado dispositivo chamando o método [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) .</span><span class="sxs-lookup"><span data-stu-id="0c1a9-115">You can get the endpoint ID for a given device by calling the [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) method.</span></span> <span data-ttu-id="0c1a9-116">Consulte a documentação da API de áudio principal para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-116">See the Core Audio API documentation for more information.</span></span>
-   <span data-ttu-id="0c1a9-117">Quando a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera dispositivos de áudio, os objetos de ativação retornados contêm esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-117">When the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function enumerates audio devices, the returned activation objects contain this attribute.</span></span> <span data-ttu-id="0c1a9-118">O atributo é usado internamente pelo objeto de ativação quando cria a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-118">The attribute is used internally by the activation object when it creates the media source.</span></span>

<span data-ttu-id="0c1a9-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0c1a9-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1a9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c1a9-120">Requirements</span></span>



| <span data-ttu-id="0c1a9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c1a9-121">Requirement</span></span> | <span data-ttu-id="0c1a9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0c1a9-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1a9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c1a9-123">Header</span></span><br/> | <dl> <span data-ttu-id="0c1a9-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1a9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c1a9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c1a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1a9-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c1a9-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c1a9-127">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="0c1a9-127">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="0c1a9-128">Capturar atributos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="0c1a9-128">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 
