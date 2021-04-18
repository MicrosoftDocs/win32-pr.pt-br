---
description: Especifica o número máximo de quadros que a fonte de captura de vídeo armazenará em buffer.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788140"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>\_Tipo de fonte de atributo DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ \_ atributo Max buffers

Especifica o número máximo de quadros que a fonte de captura de vídeo armazenará em buffer.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Por padrão, a fonte de captura de vídeo armazena em buffer um máximo de um quadro por vez. Você pode aumentar o limite de buffer definindo esse atributo.

A maneira correta de definir esse atributo depende da função usada para criar a origem da mídia:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): defina o atributo por meio do parâmetro *pAttributes* da função.
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): defina o atributo por meio do parâmetro *pAttributes* da função.
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): defina o atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornado pela função. Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

O atributo aplica-se somente a dispositivos de captura de vídeo.

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

 

 




