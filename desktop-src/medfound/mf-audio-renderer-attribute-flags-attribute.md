---
description: Contém sinalizadores para configurar o renderador de áudio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1146ce4e363dca63819badd96abcd9d9e91051419df3b5007c237a002bb39d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105002"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ FLAGS

Contém sinalizadores para configurar o renderador de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um **OR** bit a bit dos sinalizadores a seguir.



| Valor                                                   | Descrição                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SINALIZADORES DE ATRIBUTO DO RENDERADOR DE ÁUDIO MF \_ \_ \_ \_ \_ CROSSPROCESS** | O renderador de áudio usa uma sessão de áudio entre processos. Esse sinalizador permite que renderadores de áudio em vários processos compartilhem a mesma sessão de áudio, juntamente com os controles de política e volume associados.<br/> Se esse sinalizador não estiver definido, a sessão de áudio não poderá ser compartilhada por renderadores de áudio em outros processos.<br/> |
| **\_ \_ NOPERSIST DE \_ SINALIZADORES DE ATRIBUTO DO RENDERADOR DE \_ ÁUDIO \_ MF**    | A API Windows de sessão de áudio (WASAPI) não manterá as propriedades dessa sessão de áudio, como o volume da sessão.<br/> Se esse sinalizador não estiver definido, WASAPI persistirá as propriedades da sessão de áudio.<br/>                                                                                                       |



 

Você pode usar esse atributo para configurar o renderador de áudio. O uso depende de qual função você chama para criar o renderdor de áudio:

-   [**MFCreateAudioRenderer:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)de definir esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes.*
-   [**MFCreateAudioRendererActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate)de definir esse atributo usando o ponteiro da interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no *parâmetro ppActivate.* De definir o atributo antes de [**chamar IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Renderização de áudio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 




