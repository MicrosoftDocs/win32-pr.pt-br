---
description: Contém sinalizadores para configurar o processador de áudio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760298"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a>\_Atributo de \_ sinalizadores de atributo de processamento de áudio MF \_ \_

Contém sinalizadores para configurar o processador de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é uma operação bit a bit **ou** dos sinalizadores a seguir.



| Valor                                                   | Descrição                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_sinalizadores de atributo do processador de áudio MF \_ \_ \_ \_ CROSSPROCESS** | O processador de áudio usa uma sessão de áudio de processo cruzado. Esse sinalizador permite que os renderizadores de áudio em vários processos compartilhem a mesma sessão de áudio, juntamente com os controles de política e de volume associados.<br/> Se esse sinalizador não for definido, a sessão de áudio não poderá ser compartilhada por renderizadores de áudio em outros processos.<br/> |
| **\_sinalizadores de atributo do processador de áudio MF \_ \_ \_ \_ nopersist**    | A API de sessão de áudio do Windows (WASAPI) não manterá as propriedades desta sessão de áudio, como o volume da sessão.<br/> Se esse sinalizador não for definido, WASAPI manterá as propriedades de sessão de áudio.<br/>                                                                                                       |



 

Você pode usar esse atributo para configurar o processador de áudio. O uso depende de qual função você chama para criar o processador de áudio:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* . Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

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

 

 




