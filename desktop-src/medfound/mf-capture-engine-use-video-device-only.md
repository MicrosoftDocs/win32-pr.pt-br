---
description: Especifica se o mecanismo de captura captura vídeo, mas não áudio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Atributo MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921277"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>\_Mecanismo de captura MF usar o \_ \_ \_ \_ \_ atributo somente dispositivo de vídeo

Especifica se o mecanismo de captura captura vídeo, mas não áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o mecanismo de captura não selecionará nem usará um dispositivo de captura de áudio. Defina esse atributo como **true** se desejar capturar vídeo sem áudio. O valor padrão é **false**.

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

 

 




