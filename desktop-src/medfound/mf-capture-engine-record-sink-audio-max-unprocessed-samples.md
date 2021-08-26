---
description: Define o número máximo de amostras não processadas que podem ser armazenados em buffer para processamento no caminho de áudio do record sink.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060826"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>Atributo MF \_ CAPTURE ENGINE RECORD SINK AUDIO MAX \_ \_ \_ \_ \_ \_ UNPROCESSED \_ SAMPLES

Define o número máximo de amostras não processadas que podem ser armazenados em buffer para processamento no caminho de áudio do record sink.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

O valor máximo para esse atributo é 100.

Depois que o registro tiver armazenado em buffer o número máximo de amostras não processadas, especificadas por AMOSTRAS NÃO PROCESSADAS DE ÁUDIO MÁX. DE ÁUDIO MÁX. DO SINK DO MF CAPTURE ENGINE, ele descarta a taxa de quadros descartando \_ \_ \_ \_ \_ \_ \_ \_ amostras.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Mecanismo de Captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




