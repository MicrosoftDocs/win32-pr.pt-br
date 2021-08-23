---
description: Contém o link simbólico para um driver de captura de vídeo.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104942"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATRIBUTO SOURCE TYPE \_ \_ \_ VIDCAP \_ SYMBOLIC \_ LINK

Contém o link simbólico para um driver de captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**Wchar\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Use esse atributo como entrada para a [**função MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)

Além disso, esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

O link simbólico deve ser considerado uma cadeia de caracteres opaca. O nome de exibição acessível por humanos para um dispositivo está contido no atributo [MF \_ DEVSOURCE \_ ATTRIBUTE FRIENDLY \_ \_ NAME.](mf-devsource-attribute-friendly-name.md)

O atributo MF DEVSOURCE ATTRIBUTE SOURCE TYPE VIDCAP SYMBOLIC LINK pode ser passado como o valor do argumento DevicePath da \_ \_ função \_ \_ \_ \_ \_ [**SetupDiOpenDeviceInterface.**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
