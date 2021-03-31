---
description: Especifica se o mecanismo de captura captura áudio, mas não vídeo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Atributo MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921031"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>\_Mecanismo de captura MF usar o \_ \_ \_ \_ \_ atributo somente dispositivo de áudio

Especifica se o mecanismo de captura captura áudio, mas não vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o mecanismo de captura não selecionará nem usará um dispositivo de captura de vídeo. Defina esse atributo como **true** se você quiser capturar áudio sem vídeo. O valor padrão é **false**.

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

 

 




