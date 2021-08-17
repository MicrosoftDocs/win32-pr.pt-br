---
description: Especifica se o fluxo de imagem em uma origem de captura de vídeo é independente do fluxo de vídeo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Atributo MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52392839c5f196159692bc9c4624cbda67b869471d6737c4cff60c847f890e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956676"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a>\_Atributo de \_ \_ fluxo de imagem independente MF DEVICESTREAM \_

Especifica se o fluxo de imagem em uma origem de captura de vídeo é independente do fluxo de vídeo.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Algumas câmeras de vídeo USB expõem um fluxo que produz imagens ainda. Em algumas câmeras, o fluxo de imagem simplesmente retorna o próximo quadro do fluxo de vídeo. Em outras câmeras, o fluxo de imagens funciona independentemente do fluxo de vídeo. Se a câmera tiver um fluxo de imagem independente, a origem da mídia para o dispositivo de captura definirá esse atributo como **true** no fluxo da imagem.

Para obter esse atributo, faça o seguinte:

1.  Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.
3.  Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.

Esse atributo se aplica somente quando o atributo de [ \_ \_ \_ fluxo de imagem DEVICESTREAM MF](mf-devicestream-image-stream.md) é **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




