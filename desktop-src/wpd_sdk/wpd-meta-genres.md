---
description: O \_ tipo de \_ Enumeração metagêneros WPD descreve um tipo de gênero amplo de um arquivo de mídia.
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: Enumeração de WPD_META_GENRES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813421"
---
# <a name="wpd_meta_genres-enumeration"></a>\_Enumeração de \_ contragêneros WPD

O tipo de enumeração **\_ \_ metagêneros WPD** descreve um tipo de gênero amplo de um arquivo de mídia.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_gênero meta de WPD \_ \_ não utilizado**
</dt> <dd>

O gênero não foi definido ou não é aplicável.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_arquivo de \_ \_ áudio de \_ música genérico do \_ gênero \_ do meta WPD**
</dt> <dd>

Este é um arquivo de música genérico (somente áudio).

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_arquivo de \_ \_ \_ \_ áudio não musical \_ \_ genérico do gênero de um título WPD**
</dt> <dd>

Este é um arquivo de áudio genérico não musical, por exemplo, um livro de fala ou áudio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_ \_ \_ \_ \_ \_ os arquivos de livro de áudio da palavra FALAda do gênero \_ do título WPD**
</dt> <dd>

Este é um arquivo de livro de áudio.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**metagênero do \_ título WPD \_ \_ falado \_ arquivos do Word \_ \_ sem \_ áudio \_**
</dt> <dd>

Este é um arquivo de áudio de palavras falados que não é um livro de áudio, por exemplo, uma entrevista ou uma fala.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_ \_ manchete do metagênero de WPD \_ falado do \_ Word \_**
</dt> <dd>

Este é um arquivo de notícias ou de vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**metagênero do \_ título WPD \_ \_ falado pelo \_ Word \_ Talk \_**
</dt> <dd>

Esta é uma gravação de áudio de um programa de conversa.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_arquivo de \_ \_ vídeo genérico \_ do gênero do meta de \_ WPD**
</dt> <dd>

Este é um arquivo de vídeo genérico.

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_arquivo de \_ \_ vídeo de notícias de metagênero WPD \_ \_**
</dt> <dd>

Este é um arquivo de vídeo de notícias.

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_arquivo de \_ vídeo de música do gênero do título WPD \_ \_ \_**
</dt> <dd>

Este é um arquivo de vídeo de música.

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_arquivo de \_ vídeo de início do gênero do título WPD \_ \_ \_**
</dt> <dd>

Este é um arquivo de vídeo inicial.

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_arquivo de \_ \_ vídeo de filme do recurso de metagênero WPD \_ \_ \_**
</dt> <dd>

Este é um arquivo de vídeo de filme de recurso.

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_arquivo de \_ vídeo de televisão do gênero do meta WPD \_ \_ \_**
</dt> <dd>

Este é um arquivo de vídeo do programa de televisão.

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_arquivo de \_ \_ \_ vídeo Educative de treinamento \_ de \_ título WPD**
</dt> <dd>

Este é um arquivo de vídeo educacional.

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_arquivo de \_ \_ vídeo de montagem de foto do gênero \_ do \_ título WPD \_**
</dt> <dd>

Este é um arquivo de vídeo com uma montagem de foto.

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**o \_ metagênero de WPD genérico de não \_ \_ \_ \_ áudio \_ não \_ vídeo**
</dt> <dd>

Este é um arquivo sem áudio ou vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_podcast de \_ áudio do gênero do título WPD \_ \_**
</dt> <dd>

Este é um podcast de áudio.

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast de \_ vídeo do gênero meta \_ WPD \_**
</dt> <dd>

Este é um podcast em vídeo.

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_podcast de \_ metagênero \_ Misto \_ de WPD**
</dt> <dd>

Este é um podcast que contém áudio e vídeo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ \_ metagênero de mídia WPD](media-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




