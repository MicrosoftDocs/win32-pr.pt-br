---
description: Especifica se o Mecanismo de Mídia reproduzirá o conteúdo protegido.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956436"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>Atributo MF \_ MEDIA ENGINE CONTENT PROTECTION \_ \_ \_ \_ FLAGS

Especifica se o Mecanismo de Mídia reproduzirá o conteúdo protegido.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um **OR** bit a bit de sinalizadores da [**enumeração MF \_ MEDIA ENGINE PROTECTION \_ \_ \_ FLAGS.**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) Para habilitar a reprodução de conteúdo protegido, de definir o **sinalizador \_ \_ \_ \_ HABILITAR \_** CONTEÚDO PROTEGIDO DO MECANISMO DE MÍDIA do MF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Mecanismo de Mídia](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




