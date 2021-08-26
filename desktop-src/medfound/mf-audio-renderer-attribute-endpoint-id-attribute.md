---
description: Especifica o identificador do dispositivo de ponto de extremidade de áudio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dd99a42442342e25c748e12f8af84a03f2322b8c3dd24bb915b50b57952d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941126"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ ENDPOINT \_ ID

Especifica o identificador do dispositivo de ponto de extremidade de áudio.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para configurar o renderador de áudio. O uso depende de qual função você chama para criar o renderdor de áudio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)de definir esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)de definir esse atributo usando o ponteiro da interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no *parâmetro ppActivate.* De definir o atributo antes de [**chamar IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Um dispositivo de ponto de extremidade de áudio é um dispositivo de hardware que está em uma extremidade de um caminho de dados de áudio, como um fone de ouvido ou um alto-falante. Para obter o identificador do ponto de extremidade de áudio, use as seguintes APIs de áudio principais:

-   Use a interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) para enumerar os dispositivos no sistema.
-   Chame [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador do dispositivo.

Para obter mais informações, consulte a [documentação da](../coreaudio/core-audio-apis-in-windows-vista.md) API de Áudio Principal. Se esse atributo não estiver definido, o renderador de áudio usará o dispositivo de ponto de extremidade padrão.

Se esse atributo estiver definido, não de definido o atributo FUNÇÃO DE PONTO DE EXTREMIDADE DO ATRIBUTO DO [**\_ \_ RENDERADOR \_ \_ \_**](mf-audio-renderer-attribute-endpoint-role-attribute.md) DE ÁUDIO MF. Se ambos os atributos estão definidos, ocorrerá uma falha quando o renderdor de áudio for criado.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do renderador de áudio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Renderização de áudio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
