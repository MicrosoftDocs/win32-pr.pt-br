---
description: Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de vídeo do coletor de registros.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Atributo MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f776dd795103fccf81da4c739b767131a03bf83245c3c79e724274dcb52dc0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956816"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>\_Mecanismo de captura MF registro do coletor de \_ \_ \_ \_ vídeo máximo de amostras não \_ \_ processadas \_

Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de vídeo do coletor de registros.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

O valor máximo para esse atributo é 17.

Depois que o registro tiver armazenado em buffer o número máximo de amostras não processadas, especificado pelo \_ mecanismo de captura MF registro do coletor de \_ \_ \_ \_ vídeo \_ máximo amostras não \_ processadas \_ , ele descartará a taxa de quadros soltando amostras.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




