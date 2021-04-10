---
description: Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de áudio do coletor de registros.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Atributo MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296565"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>\_Registro do mecanismo de captura MF máximo do atributo de \_ \_ \_ \_ \_ \_ amostras não processadas do áudio do coletor \_

Define o número máximo de amostras não processadas que podem ser armazenadas em buffer para processamento no caminho de áudio do coletor de registros.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

O valor máximo para esse atributo é 100.

Depois que o registro armazena em buffer o número máximo de amostras não processadas, especificado pelo \_ mecanismo de captura do MF \_ registro de áudio do \_ \_ coletor máximo de amostras não \_ \_ \_ processadas \_ , ele descarta a taxa de quadros soltando amostras.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




