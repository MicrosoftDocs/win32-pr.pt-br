---
description: Especifica a categoria de fluxo de áudio para o SAR (Streaming Audio Renderer).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4acb6bd0f40d3c6fb3caa6b4dce8801f8fa60d31222265d5dca6ff5a132444e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714876"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a>Atributo MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE STREAM \_ \_ CATEGORY

Especifica a categoria de fluxo de áudio para o SAR [(Streaming Audio Renderer).](streaming-audio-renderer.md)

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Você pode usar esse atributo para configurar o renderador de áudio. O uso depende de qual função você chama para criar o renderdor de áudio.



| Função                                                               | Como definir o atributo                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | Use o [**ponteiro IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no *parâmetro pAudioAttributes.*                                                                                          |
| [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | Use o [**ponteiro IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornado no *parâmetro ppActivate.* De definir o atributo antes de [**chamar IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). |



 

O valor do atributo é um membro da [**enumeração CATEGORIA \_ DE FLUXO \_ DE**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) ÁUDIO. O serviço de áudio usa a categoria de fluxo para determinar políticas de áudio quando vários aplicativos tocam áudio ao mesmo tempo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
