---
description: O \_ tipo de enumeração de tipos de dispositivos WPD \_ descreve os diferentes tipos de dispositivo portátil do Windows (wpd) comumente usados para determinar a classificação básica e a aparência visual de um dispositivo portátil.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Enumeração de WPD_DEVICE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770648"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="9a701-103">Enumeração de tipos de \_ dispositivos WPD \_</span><span class="sxs-lookup"><span data-stu-id="9a701-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="9a701-104">O tipo de enumeração de **\_ \_ tipos de dispositivos WPD** descreve os diferentes tipos de dispositivo portátil do Windows (wpd) comumente usados para determinar a classificação básica e a aparência visual de um dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="9a701-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a701-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a701-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="9a701-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9a701-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9a701-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_tipo de dispositivo WPD \_ \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="9a701-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-108">Um WPD genérico que inclui dispositivos multifuncionais que não se enquadram em um dos outros valores de enumeração de [**\_ \_ tipos de dispositivos WPD**](wpd-device-types.md) .</span><span class="sxs-lookup"><span data-stu-id="9a701-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_câmera do \_ tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-110">Um dispositivo de câmera, como uma câmera digital ainda.</span><span class="sxs-lookup"><span data-stu-id="9a701-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_player de \_ mídia do tipo de dispositivo WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-112">Um dispositivo de player de mídia que dá suporte à reprodução de imagens de áudio, vídeo ou exibição, como um player portátil de música ou Portable Media Center.</span><span class="sxs-lookup"><span data-stu-id="9a701-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="9a701-113">Nem todas essas funções são classificadas como um player de \_ mídia do tipo de dispositivo WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a701-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="9a701-114">Por exemplo, os dispositivos de player de música portáteis são classificados como \_ player de mídia do tipo de dispositivo WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a701-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_telefone do \_ tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-116">Um dispositivo de telefone, como um telefone celular.</span><span class="sxs-lookup"><span data-stu-id="9a701-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_vídeo do \_ tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-118">Um dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a701-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_Gerenciador de \_ \_ informações pessoais \_ do tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-120">Um dispositivo do Gerenciador de informações pessoais.</span><span class="sxs-lookup"><span data-stu-id="9a701-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="9a701-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_gravador de \_ áudio do tipo de dispositivo WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9a701-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="9a701-122">Um dispositivo de gravador de áudio.</span><span class="sxs-lookup"><span data-stu-id="9a701-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a701-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a701-123">Remarks</span></span>

<span data-ttu-id="9a701-124">**WPD \_ Os \_ tipos de dispositivo** são lidos usando a interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="9a701-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="9a701-125">Os aplicativos WPD podem usar esses valores para determinar a aparência visual genérica do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a701-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="9a701-126">Ou seja, uma imagem de câmera é exibida para dispositivos semelhantes a câmeras, uma imagem de telefone celular é exibida para dispositivos semelhantes ao telefone e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9a701-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="9a701-127">Os aplicativos WPD devem usar os recursos do dispositivo portátil para determinar a função, não o valor dos **\_ \_ tipos de dispositivos WPD** .</span><span class="sxs-lookup"><span data-stu-id="9a701-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a701-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a701-128">Requirements</span></span>



| <span data-ttu-id="9a701-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a701-129">Requirement</span></span> | <span data-ttu-id="9a701-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9a701-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a701-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a701-131">Header</span></span><br/> | <dl> <span data-ttu-id="9a701-132"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a701-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a701-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a701-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a701-134">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="9a701-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




