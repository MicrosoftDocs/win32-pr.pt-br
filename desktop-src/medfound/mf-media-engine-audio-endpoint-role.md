---
description: Especifica a função de dispositivo para o fluxo de áudio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105788987"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
