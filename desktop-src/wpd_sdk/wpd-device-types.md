---
description: o \_ tipo de enumeração de tipos de dispositivos wpd \_ descreve os diferentes tipos de Windows dispositivos portáteis (WPD) comumente usados para determinar a classificação básica e a aparência visual de um dispositivo portátil.
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
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657456"
---
# <a name="wpd_device_types-enumeration"></a>Enumeração de tipos de \_ dispositivos WPD \_

o tipo de enumeração de **\_ \_ tipos de dispositivos wpd** descreve os diferentes tipos de Windows dispositivos portáteis (WPD) comumente usados para determinar a classificação básica e a aparência visual de um dispositivo portátil.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_tipo de dispositivo WPD \_ \_ genérico**
</dt> <dd>

Um WPD genérico que inclui dispositivos multifuncionais que não se enquadram em um dos outros valores de enumeração de [**\_ \_ tipos de dispositivos WPD**](wpd-device-types.md) .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_câmera do \_ tipo de dispositivo WPD \_**
</dt> <dd>

Um dispositivo de câmera, como uma câmera digital ainda.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_player de \_ mídia do tipo de dispositivo WPD \_ \_**
</dt> <dd>

Um dispositivo de player de mídia que dá suporte à reprodução de imagens de áudio, vídeo ou exibição, como um player portátil de música ou Portable Media Center. Nem todas essas funções são classificadas como um player de \_ mídia do tipo de dispositivo WPD \_ \_ \_ . Por exemplo, os dispositivos de player de música portáteis são classificados como \_ player de mídia do tipo de dispositivo WPD \_ \_ \_ .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**\_telefone do \_ tipo de dispositivo WPD \_**
</dt> <dd>

Um dispositivo de telefone, como um telefone celular.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_vídeo do \_ tipo de dispositivo WPD \_**
</dt> <dd>

Um dispositivo de vídeo.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_Gerenciador de \_ \_ informações pessoais \_ do tipo de dispositivo WPD \_**
</dt> <dd>

Um dispositivo do Gerenciador de informações pessoais.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_gravador de \_ áudio do tipo de dispositivo WPD \_ \_**
</dt> <dd>

Um dispositivo de gravador de áudio.

</dd> </dl>

## <a name="remarks"></a>Comentários

**WPD \_ Os \_ tipos de dispositivo** são lidos usando a interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) . Os aplicativos WPD podem usar esses valores para determinar a aparência visual genérica do dispositivo. Ou seja, uma imagem de câmera é exibida para dispositivos semelhantes a câmeras, uma imagem de telefone celular é exibida para dispositivos semelhantes ao telefone e assim por diante.

> [!Note]  
> Os aplicativos WPD devem usar os recursos do dispositivo portátil para determinar a função, não o valor dos **\_ \_ tipos de dispositivos WPD** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




