---
description: Especifica o formato de saída de um dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Atributo MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105759845"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>\_Atributo de \_ tipo de mídia de atributo MF DEVSOURCE \_ \_

Especifica o formato de saída de um dispositivo.

## <a name="data-type"></a>Tipo de dados

**[**MFT \_ \_ \_ Informações de tipo de registro**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** armazenadas como **byte \[ \]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentários

Este atributo contém um par de GUIDs: um tipo principal e um subtipo. Essas GUIDs descrevem o formato de saída padrão do dispositivo. O dispositivo pode dar suporte a formatos de saída adicionais.

Por exemplo, se um dispositivo de captura de vídeo produzir vídeo RGB-32, o valor desse atributo será `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Esse atributo é uma dica para o aplicativo. Para obter o formato de saída exato, crie a origem da mídia para o dispositivo e obtenha o descritor de apresentação da origem de mídia.

Esse atributo é definido nos objetos de ativação retornados pelas seguintes funções:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

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

 

 




