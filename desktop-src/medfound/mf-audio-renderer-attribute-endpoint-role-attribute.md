---
description: Especifica a função de ponto de extremidade de áudio para o processador de áudio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922075"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a>\_Atributo de \_ função de \_ ponto de extremidade de atributo de processamento \_ de áudio \_ MF

Especifica a função de ponto de extremidade de áudio para o processador de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para configurar o processador de áudio. O uso depende de qual função você chama para criar o processador de áudio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* . Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

Um dispositivo de ponto de extremidade de áudio é um dispositivo de hardware que está em uma extremidade de um caminho de dados de áudio, como um fone de ouvido ou um palestrante.

Se esse atributo for definido, o processador de áudio usará o dispositivo de áudio padrão para a função especificada. O valor desse atributo é um membro da enumeração **ERole** , que é definida no arquivo de cabeçalho mmdeviceapi. h. Para obter mais informações, consulte a documentação da API de áudio principal. Se esse atributo não for definido, o processador de áudio usará o dispositivo de ponto de extremidade padrão.

Se esse atributo estiver definido, não defina o atributo [**de \_ ID do \_ ponto de extremidade do atributo de processador \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) . Se ambos os atributos forem definidos, ocorrerá uma falha quando o processador de áudio for criado.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 




