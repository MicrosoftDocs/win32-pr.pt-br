---
description: Especifica o perfil de codificação de vídeo no tipo de mídia de saída. Este é um alias do \_ atributo de perfil MF mt de \_ MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Atributo MF_MT_VIDEO_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d2af7c6ebbbbb78626e96385a6eda5a25c38a3ae8473fac866866248570cc48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741389"
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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
