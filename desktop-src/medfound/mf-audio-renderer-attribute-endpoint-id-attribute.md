---
description: Especifica o identificador para o dispositivo de ponto de extremidade de áudio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296568"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a>\_Atributo de \_ ID do \_ ponto de extremidade do atributo de processamento \_ de áudio \_ MF

Especifica o identificador para o dispositivo de ponto de extremidade de áudio.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para configurar o processador de áudio. O uso depende de qual função você chama para criar o processador de áudio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* . Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Um dispositivo de ponto de extremidade de áudio é um dispositivo de hardware que está em uma extremidade de um caminho de dados de áudio, como um fone de ouvido ou um palestrante. Para obter o identificador de ponto de extremidade de áudio, use as seguintes APIs de áudio principal:

-   Use a interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) para enumerar os dispositivos no sistema.
-   Chame [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador para o dispositivo.

Para obter mais informações, consulte a documentação da API de [áudio principal](../coreaudio/core-audio-apis-in-windows-vista.md) . Se esse atributo não for definido, o processador de áudio usará o dispositivo de ponto de extremidade padrão.

Se esse atributo estiver definido, não defina o atributo [**de \_ função de \_ ponto de extremidade do atributo de processamento \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) . Se ambos os atributos forem definidos, ocorrerá uma falha quando o processador de áudio for criado.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do processador de áudio](audio-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
