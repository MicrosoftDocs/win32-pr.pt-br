---
description: Especifica a função de dispositivo para o fluxo de áudio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a15a973aef342e3d37cde3e6d9f3dd7d61c553fecaa943215dbcc77a319950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104772"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>\_Atributo de \_ função de \_ ponto de extremidade de áudio do mecanismo \_ de mídia \_ MF

Especifica a função de dispositivo para o fluxo de áudio.

## <a name="data-type"></a>Tipo de dados

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .

Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia. O atributo é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
