---
description: Especifica se o mecanismo de captura captura áudio, mas não vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Atributo MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c248923ae2dce7d5153f8e88cb8eef88d29ea3dbf6ce5c94e4a8ee355af16c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013346"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>\_Mecanismo de captura MF usar o \_ \_ \_ \_ \_ atributo somente dispositivo de áudio

Especifica se o mecanismo de captura captura áudio, mas não vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o mecanismo de captura não selecionará nem usará um dispositivo de captura de vídeo. Defina esse atributo como **true** se você quiser capturar áudio sem vídeo. O valor padrão é **FALSE**.

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

 

 




