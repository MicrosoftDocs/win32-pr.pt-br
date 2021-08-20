---
description: Especifica se uma fonte de captura de vídeo é um dispositivo de hardware ou um dispositivo de software.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399a486c5637cb617aec0570daa673db5b07874747f8ee9caae359f94087b5a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060720"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a>\_Tipo de origem de atributo MF DEVSOURCE, atributo de \_ \_ \_ \_ \_ origem HW VIDCAP \_

Especifica se uma fonte de captura de vídeo é um dispositivo de hardware ou um dispositivo de software.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Se o valor for **true**, a origem da captura será um dispositivo de hardware. Se o valor for **false**, ele será um dispositivo de software. O valor padrão é **FALSE**.

Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

O atributo aplica-se somente a dispositivos de captura de vídeo.

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

 

 




