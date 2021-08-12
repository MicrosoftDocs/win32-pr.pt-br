---
description: Define o número máximo de amostras processadas que podem ser armazenados em buffer no caminho de áudio do sink de registro.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b4478ebecfc873c612e8deb0106cba5462e77cd56d5d818b03d74e88679c8b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245034"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a>Atributo AMOSTRAS PROCESSADAS DE \_ \_ ÁUDIO \_ \_ \_ \_ MÁX. \_ \_ DE REGISTRO DO MECANISMO DE CAPTURA DE MF

Define o número máximo de amostras processadas que podem ser armazenados em buffer no caminho de áudio do sink de registro.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Para configurar esse atributo no mecanismo de captura, adicione-o ao parâmetro *pAttributes* ao chamar [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

O valor máximo para esse atributo é 100.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Mecanismo de Captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




