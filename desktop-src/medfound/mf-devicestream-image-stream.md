---
description: Especifica se um fluxo em uma origem de captura de vídeo é um fluxo de imagem ainda.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Atributo MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a42ec0ea6ac8f89c7b35e5ae137c92aaf62006b9b06be689bb7203626f36b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244759"
---
# <a name="mf_devicestream_image_stream-attribute"></a>\_Atributo de \_ fluxo de imagem DEVICESTREAM MF \_

Especifica se um fluxo em uma origem de captura de vídeo é um fluxo de imagem ainda.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Algumas câmeras de vídeo expõem um fluxo de imagem ainda que produz imagens de alta resolução. O fluxo de imagem pode produzir imagens descompactadas ou imagens JPEG. Se a câmera tiver um fluxo de imagem, a origem da mídia para o dispositivo de captura definirá esse atributo como **true** no fluxo da imagem.

Para obter esse atributo, faça o seguinte:

1.  Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.
3.  Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




