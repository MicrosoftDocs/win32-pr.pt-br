---
description: Especifica a ID do ponto de extremidade para um dispositivo de captura de áudio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baafd2aa1bdfc3f4959b877963faff5df9aabe57c672555edb98f4cded8b1ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113946"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATRIBUTO SOURCE TYPE \_ \_ \_ AUDCAP \_ ENDPOINT \_ ID attribute

Especifica a ID do ponto de extremidade para um dispositivo de captura de áudio.

## <a name="data-type"></a>Tipo de dados

**Wchar\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

O valor do atributo é uma ID de ponto de extremidade. Esse atributo é usado com as seguintes funções:

-   Ele pode ser usado como entrada para as funções [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) Nesse contexto, o atributo especifica o dispositivo de captura de áudio para a função. Você pode obter a ID do ponto de extremidade para um determinado dispositivo chamando o [**método IMMDevice::GetId.**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) Confira a documentação da API de Áudio Principal para obter mais informações.
-   Quando a [**função MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera dispositivos de áudio, os objetos de ativação retornados contêm esse atributo. O atributo é usado internamente pelo objeto de ativação quando cria a fonte de mídia.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
