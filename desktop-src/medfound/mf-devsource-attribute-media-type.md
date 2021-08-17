---
description: Especifica o formato de saída de um dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105032"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE \_ MEDIA \_ TYPE

Especifica o formato de saída de um dispositivo.

## <a name="data-type"></a>Tipo de dados

**[**MFT \_ REGISTRAR \_ INFORMAÇÕES \_ DE TIPO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** armazenadas como **BYTE \[ \]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Para definir esse atributo, chame [**IMFAttributes::SetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Comentários

Esse atributo contém um par de GUIDs: um tipo principal e um subtipo. Esses GUIDs descrevem o formato de saída padrão do dispositivo. O dispositivo pode dar suporte a formatos de saída adicionais.

Por exemplo, se um dispositivo de captura de vídeo tiver saída de vídeo RGB-32, o valor desse atributo será `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Esse atributo é uma dica para o aplicativo. Para obter o formato de saída exato, crie a fonte de mídia para o dispositivo e obter o descritor de apresentação da fonte de mídia.

Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

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

 

 




