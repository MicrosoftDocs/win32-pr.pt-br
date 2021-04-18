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
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ atributo ID do ponto de extremidade \_

Especifica a ID do ponto de extremidade para um dispositivo de captura de áudio.

## <a name="data-type"></a>Tipo de dados

**WCHAR\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

O valor do atributo é uma ID de ponto de extremidade. Esse atributo é usado com as seguintes funções:

-   Ele pode ser usado como entrada para as funções [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Nesse contexto, o atributo especifica o dispositivo de captura de áudio para a função. Você pode obter a ID do ponto de extremidade para um determinado dispositivo chamando o método [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) . Consulte a documentação da API de áudio principal para obter mais informações.
-   Quando a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera dispositivos de áudio, os objetos de ativação retornados contêm esse atributo. O atributo é usado internamente pelo objeto de ativação quando cria a origem da mídia.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
