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
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="c1035-103">\_Enumeração de \_ contragêneros WPD</span><span class="sxs-lookup"><span data-stu-id="c1035-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="c1035-104">O tipo de enumeração **\_ \_ metagêneros WPD** descreve um tipo de gênero amplo de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c1035-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1035-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1035-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="c1035-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c1035-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1035-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_gênero meta de WPD \_ \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="c1035-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-108">O gênero não foi definido ou não é aplicável.</span><span class="sxs-lookup"><span data-stu-id="c1035-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**\_arquivo de \_ \_ áudio de \_ música genérico do \_ gênero \_ do meta WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-110">Este é um arquivo de música genérico (somente áudio).</span><span class="sxs-lookup"><span data-stu-id="c1035-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="c1035-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**\_arquivo de \_ \_ \_ \_ áudio não musical \_ \_ genérico do gênero de um título WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-112">Este é um arquivo de áudio genérico não musical, por exemplo, um livro de fala ou áudio.</span><span class="sxs-lookup"><span data-stu-id="c1035-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**\_ \_ \_ \_ \_ \_ os arquivos de livro de áudio da palavra FALAda do gênero \_ do título WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-114">Este é um arquivo de livro de áudio.</span><span class="sxs-lookup"><span data-stu-id="c1035-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**metagênero do \_ título WPD \_ \_ falado \_ arquivos do Word \_ \_ sem \_ áudio \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-116">Este é um arquivo de áudio de palavras falados que não é um livro de áudio, por exemplo, uma entrevista ou uma fala.</span><span class="sxs-lookup"><span data-stu-id="c1035-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**\_ \_ manchete do metagênero de WPD \_ falado do \_ Word \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-118">Este é um arquivo de notícias ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1035-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**metagênero do \_ título WPD \_ \_ falado pelo \_ Word \_ Talk \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-120">Esta é uma gravação de áudio de um programa de conversa.</span><span class="sxs-lookup"><span data-stu-id="c1035-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**\_arquivo de \_ \_ vídeo genérico \_ do gênero do meta de \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-122">Este é um arquivo de vídeo genérico.</span><span class="sxs-lookup"><span data-stu-id="c1035-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**\_arquivo de \_ \_ vídeo de notícias de metagênero WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-124">Este é um arquivo de vídeo de notícias.</span><span class="sxs-lookup"><span data-stu-id="c1035-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**\_arquivo de \_ vídeo de música do gênero do título WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-126">Este é um arquivo de vídeo de música.</span><span class="sxs-lookup"><span data-stu-id="c1035-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**\_arquivo de \_ vídeo de início do gênero do título WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-128">Este é um arquivo de vídeo inicial.</span><span class="sxs-lookup"><span data-stu-id="c1035-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**\_arquivo de \_ \_ vídeo de filme do recurso de metagênero WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-130">Este é um arquivo de vídeo de filme de recurso.</span><span class="sxs-lookup"><span data-stu-id="c1035-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**\_arquivo de \_ vídeo de televisão do gênero do meta WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-132">Este é um arquivo de vídeo do programa de televisão.</span><span class="sxs-lookup"><span data-stu-id="c1035-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**\_arquivo de \_ \_ \_ vídeo Educative de treinamento \_ de \_ título WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-134">Este é um arquivo de vídeo educacional.</span><span class="sxs-lookup"><span data-stu-id="c1035-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**\_arquivo de \_ \_ vídeo de montagem de foto do gênero \_ do \_ título WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-136">Este é um arquivo de vídeo com uma montagem de foto.</span><span class="sxs-lookup"><span data-stu-id="c1035-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**o \_ metagênero de WPD genérico de não \_ \_ \_ \_ áudio \_ não \_ vídeo**</span><span class="sxs-lookup"><span data-stu-id="c1035-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-138">Este é um arquivo sem áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1035-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**\_podcast de \_ áudio do gênero do título WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-140">Este é um podcast de áudio.</span><span class="sxs-lookup"><span data-stu-id="c1035-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**\_podcast de \_ vídeo do gênero meta \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c1035-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-142">Este é um podcast em vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1035-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="c1035-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**\_podcast de \_ metagênero \_ Misto \_ de WPD**</span><span class="sxs-lookup"><span data-stu-id="c1035-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="c1035-144">Este é um podcast que contém áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1035-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1035-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1035-145">Remarks</span></span>

<span data-ttu-id="c1035-146">Essa enumeração é usada pela propriedade [de \_ \_ \_ metagênero de mídia WPD](media-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c1035-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1035-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1035-147">Requirements</span></span>



| <span data-ttu-id="c1035-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1035-148">Requirement</span></span> | <span data-ttu-id="c1035-149">Valor</span><span class="sxs-lookup"><span data-stu-id="c1035-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1035-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1035-150">Header</span></span><br/> | <dl> <span data-ttu-id="c1035-151"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1035-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1035-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1035-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1035-153">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="c1035-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




