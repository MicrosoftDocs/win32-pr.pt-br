---
description: As GUIDs a seguir definem categorias para transformações de Media Foundation (MFTs). Essas categorias são usadas para registrar e enumerar MFTs.
ms.assetid: eca3ae3b-e40a-407d-986c-d0a85b891f52
title: MFT_CATEGORY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65386561f18c105fde47d885ca97858131ecb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475552"
---
# <a name="mft_category"></a>Categoria de MFT \_

As GUIDs a seguir definem categorias para transformações de Media Foundation (MFTs). Essas categorias são usadas para registrar e enumerar MFTs.




| Constante | Descrição | 
|----------|-------------|
| <span id="MFT_CATEGORY_AUDIO_DECODER"></span><span id="mft_category_audio_decoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_DECODER</strong></dt></dl> | Decodificadores de áudio.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_EFFECT"></span><span id="mft_category_audio_effect"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_EFFECT</strong></dt></dl> | Efeitos de áudio.<br /> | 
| <span id="MFT_CATEGORY_AUDIO_ENCODER"></span><span id="mft_category_audio_encoder"></span><dl><dt><strong>MFT_CATEGORY_AUDIO_ENCODER</strong></dt></dl> | Codificadores de áudio.<br /> | 
| <span id="MFT_CATEGORY_DEMULTIPLEXER"></span><span id="mft_category_demultiplexer"></span><dl><dt><strong>MFT_CATEGORY_DEMULTIPLEXER</strong></dt></dl> | Demultiplexadores.<br /> | 
| <span id="MFT_CATEGORY_MULTIPLEXER"></span><span id="mft_category_multiplexer"></span><dl><dt><strong>MFT_CATEGORY_MULTIPLEXER</strong></dt></dl> | Multiplexadores.<br /><blockquote>[!Note]<br />no Windows Vista, o pipeline de Media Foundation não oferece suporte a MFTs com mais de uma entrada. há suporte para MFTs de várias entradas no Windows 7.</blockquote><br /><br /> | 
| <span id="MFT_CATEGORY_OTHER"></span><span id="mft_category_other"></span><dl><dt><strong>MFT_CATEGORY_OTHER</strong></dt></dl> | MFTs diversos.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_DECODER"></span><span id="mft_category_video_decoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_DECODER</strong></dt></dl> | Decodificadores de vídeo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_EFFECT"></span><span id="mft_category_video_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_EFFECT</strong></dt></dl> | Efeitos de vídeo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_RENDERER_EFFECT"></span><span id="mft_category_video_renderer_effect"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_RENDERER_EFFECT</strong></dt></dl> | Efeitos do processador de vídeo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_ENCODER"></span><span id="mft_category_video_encoder"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_ENCODER</strong></dt></dl> | Codificadores de vídeo.<br /> | 
| <span id="MFT_CATEGORY_VIDEO_PROCESSOR"></span><span id="mft_category_video_processor"></span><dl><dt><strong>MFT_CATEGORY_VIDEO_PROCESSOR</strong></dt></dl> | <blockquote>[!Note]<br />introduzido no Windows 7.</blockquote><br /> Processadores de vídeo. <br /> Essa categoria é limitada a MFTs que executam conversões de formato em vídeo descompactado, incluindo conversões de espaço de cor. Para efeitos de vídeo que modificam a aparência da imagem (como um efeito de desfoque ou uma transformação de cor para escala de cinza), use a categoria <strong>MFT_CATEGORY_VIDEO_EFFECT</strong> .<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> <dt>

[**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
</dt> </dl>

 

 




