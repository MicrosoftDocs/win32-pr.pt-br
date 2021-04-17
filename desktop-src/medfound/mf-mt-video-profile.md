---
description: Especifica o perfil de codificação de vídeo no tipo de mídia de saída. Este é um alias do \_ atributo de perfil MF mt de \_ MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Atributo MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812042"
---
# <a name="mf_mt_video_profile-attribute"></a>\_Atributo de \_ perfil de vídeo MF MT \_

Especifica o perfil de codificação de vídeo no tipo de mídia de saída. Este é um alias do atributo de [ \_ \_ \_ perfil MF mt de MPEG2](mf-mt-mpeg2-profile-attribute.md) .

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

**Codificadores H. 264:**

Os perfis com suporte são excedidos para incluir [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) e **eAVEncH264VProfile \_ ConstrainedHigh**.

Os codificadores devem dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) e [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para esse atributo.

Isso é estático, portanto, os codificadores de vídeo devem ser configurados antes do início do streaming. Se o aplicativo definir um perfil para o qual o codificador não dá suporte, o codificador deverá rejeitar o tipo de mídia.

Padrão recomendado: [**perfil \_ principal do eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
