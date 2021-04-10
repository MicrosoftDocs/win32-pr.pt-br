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
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP atributo de \_ \_ link simbólico

Contém o link simbólico para um driver de captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**WCHAR \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentários

Use esse atributo como entrada para a função [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

Além disso, esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

O link simbólico deve ser considerado uma cadeia de caracteres opaca. O nome de exibição legível por humanos de um dispositivo está contido no atributo de [ \_ \_ \_ \_ nome amigável do atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .

O atributo de DEVSOURCE MF do \_ \_ tipo de \_ origem \_ \_ VIDCAP \_ \_ de link simbólico pode ser passado como o valor do argumento DevicePath da função [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
