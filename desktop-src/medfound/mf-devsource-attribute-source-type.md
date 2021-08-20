---
description: Especifica um tipo de dispositivo, como captura de áudio ou captura de vídeo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1160242b32ce6b6b902d1575cba4d275388a38b980d69a0bad0a528f377085d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060680"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>\_Atributo de \_ tipo de fonte de atributo MF DEVSOURCE \_ \_

Especifica o tipo de um dispositivo, como captura de áudio ou captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**GUID**

Os valores a seguir são definidos para este atributo:



| Valor                                                                                                                                                                                                                                                                 | Significado                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</dt> </dl> | Dispositivo de captura de áudio.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID**</dt> </dl> | Dispositivo de captura de vídeo.<br/> |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentários

Use este atributo como entrada para as seguintes funções:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Além disso, esse atributo é definido nos objetos de ativação retornados pela função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




