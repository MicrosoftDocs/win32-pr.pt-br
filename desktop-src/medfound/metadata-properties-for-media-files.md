---
description: Este tópico lista as propriedades de metadados mais comuns para arquivos de mídia.
ms.assetid: 35187720-413a-45a0-8558-918f7c3161e1
title: Propriedades de metadados para Arquivos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cab541a480b03d7ef6bfb9a1a2036226b767774
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105782705"
---
# <a name="metadata-properties-for-media-files"></a>Propriedades de metadados para Arquivos de mídia

Este tópico lista as propriedades de metadados mais comuns para arquivos de mídia.

-   [Propriedades de mídia comuns](#common-media-properties)
-   [Propriedades de compartilhamento de mídia](#media-sharing-properties)
-   [Mapeamentos do Windows Media Format SDK](#windows-media-format-sdk-mappings)
-   [Tópicos relacionados](#related-topics)

## <a name="common-media-properties"></a>Propriedades de mídia comuns

O sistema de propriedades do Shell define um conjunto de propriedades de metadados comuns para todos os tipos de objetos do Shell. Um subconjunto deles é aplicável aos arquivos de mídia. A tabela a seguir lista as propriedades de Shell mais comuns para mídia. Os arquivos de mídia podem dar suporte a propriedades adicionais não listadas aqui. Além disso, nem todo formato de arquivo dá suporte a todas as propriedades listadas. Para obter uma lista completa das propriedades do Shell, consulte [Propriedades do Shell](/previous-versions//ff521730(v=vs.85)).



| PROPERTYKEY                                                              | Nome do Shell                                                                                    | Descrição                                                                                                                                                                                               | Tipo de Dados    |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [\_ID do \_ perfil de DLNA do conteúdo do MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md) | Nenhum                                                                                          | Identificador de perfil da rede de vida digital (DLNA).                                                                                                                                                | LPWStr do VT \_   |
| **PKEY de \_ áudio \_ ChannelCount**                                            | [System. Audio. ChannelCount](../properties/props-system-audio-channelcount.md)                       | Número de canais de áudio.                                                                                                                                                                                 | \_UI4 VT      |
| **PKEY de \_ áudio \_ EncodingBitrate**                                         | [System. Audio. EncodingBitrate](../properties/props-system-audio-encodingbitrate.md)                 | Taxa média de bits de áudio, em bits por segundo.                                                                                                                                                               | \_UI4 VT      |
| **\_Formato de áudio PKEY \_**                                                  | [System. Audio. Format](../properties/props-system-audio-format.md)                                   | Subtipo de áudio [**( \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)) expresso como uma cadeia de caracteres.                                                                                                                 | LPWStr do VT \_   |
| **PKEY de \_ áudio \_ IsVariableBitRate**                                       | [System. Audio. IsVariableBitRate](../properties/props-system-audio-isvariablebitrate.md)             | Indica se o fluxo de áudio usa codificação de taxa de bits variável.                                                                                                                                       | BOOL do VT \_     |
| **\_Picovalue de áudio PKEY \_**                                               | [System. Audio. Picovalue](../properties/props-system-audio-peakvalue.md)                             | Nível de volume de pico do conteúdo de áudio.                                                                                                                                                                       | \_UI4 VT      |
| **\_Amostra de áudio PKEY \_**                                              | [System. Audio. Sampleize](../properties/props-system-audio-samplerate.md)                           | Taxa de amostragem de áudio em amostras por segundo. Equivalente ao atributo [**MF \_ MT \_ Audio \_ Samples \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) no tipo de mídia.                           | \_UI4 VT      |
| **\_Amostras de áudio PKEY \_**                                              | [System. Audio. Sampleize](../properties/props-system-audio-samplesize.md)                           | Número de bits por amostra de áudio. Equivalente ao [**exemplo de \_ bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) no tipo de mídia.                                         | \_UI4 VT      |
| **PKEY de \_ áudio \_ StreamNumber**                                            | [System. Audio. StreamNumber](../properties/props-system-audio-streamnumber.md)                       | Identificador do fluxo de áudio.                                                                                                                                                                           | \_UI4 VT      |
| **Autor do PKEY \_**                                                         | [System.Author](../properties/props-system-author.md)                                               | Autorização.                                                                                                                                                                                                   | LPWStr do VT \_   |
| **Comentário de PKEY \_**                                                        | [Sistema. Comment](../properties/props-system-comment.md)                                             | Um comentário anexado a um arquivo, normalmente adicionado por um usuário.                                                                                                                                                  | LPWStr do VT \_   |
| **\_Direitos autorais do PKEY**                                                      | [System. Copyright](../properties/props-system-copyright.md)                                         | Informações de direitos autorais.                                                                                                                                                                                    | LPWStr do VT \_   |
| **PKEY \_ DRM \ \_ protegido**                                               | [System. DRM. isproteged](../properties/props-system-drm-isprotected.md)                             | Indica se o conteúdo é protegido usando o DRM (gerenciamento de direitos digitais).                                                                                                                         | BOOL do VT \_     |
| **\_Palavras-chave PKEY**                                                       | [System.Keywords](../properties/props-system-keywords.md)                                           | Palavras-chave.                                                                                                                                                                                                 | LPWStr do VT \_   |
| **\_Linguagem PKEY**                                                       | [System. Language](../properties/props-system-language.md)                                           | Idioma.                                                                                                                                                                                                 | LPWStr do VT \_   |
| **PKEY \_ Media \_ AuthorUrl**                                               | [System. Media. AuthorUrl](../properties/props-system-media-authorurl.md)                             | URL do site do autor.                                                                                                                                                                              | LPWStr do VT \_   |
| **PKEY \_ Media \_ AverageLevel**                                            | [System. Media. AverageLevel](../properties/props-system-media-averagelevel.md)                       | Nível médio de volume de conteúdo de áudio.                                                                                                                                                                    | \_UI4 VT      |
| **PKEY \_ Media \_ ClassPrimaryID**                                          | [System. Media. ClassPrimaryID](../properties/props-system-media-classprimaryid.md)                   | A representação de cadeia de caracteres de um GUID que identifica a classe primária de mídia. Para obter valores válidos, consulte a documentação do atributo [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md) .       | LPWStr do VT \_   |
| **PKEY \_ Media \_ ClassSecondaryID**                                        | [System. Media. ClassSecondaryID](../properties/props-system-media-classsecondaryid.md)               | A representação de cadeia de caracteres de um GUID que identifica a classe secundária de mídia. Para obter valores válidos, consulte a documentação do atributo [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md) . | LPWStr do VT \_   |
| **PKEY \_ Media \_ CollectionGroupID**                                       | [System. Media. CollectionGroupID](../properties/props-system-media-collectiongroupid.md)             | A representação de cadeia de caracteres de um GUID que identifica o grupo de coleta.                                                                                                                                 | LPWStr do VT \_   |
| **\_Conjunto de \_ coletas de mídia PKEY**                                            | [System. Media. CollectionId](../properties/props-system-media-collectionid.md)                       | A representação de cadeia de caracteres de um GUID que identifica a coleção.                                                                                                                                       | LPWStr do VT \_   |
| **PKEY \_ Media \_ ContentDistributor**                                      | [System. Media. ContentDistributor](../properties/props-system-media-contentdistributor.md)           | Distribuidor do conteúdo.                                                                                                                                                                               | LPWStr do VT \_   |
| **\_ContentId de mídia PKEY \_**                                               | [System. Media. ContentId](../properties/props-system-media-contentid.md)                             | A representação de cadeia de caracteres de um GUID que identifica a coleção.                                                                                                                                       | LPWStr do VT \_   |
| **PKEY \_ Media \_ DateEncoded**                                             | [System. Media. DateEncoded](../properties/props-system-media-dateencoded.md)                         | Hora em que o conteúdo foi codificado.                                                                                                                                                                        | FILETIME do VT \_ |
| **PKEY \_ Media \_ DateReleased**                                            | [System. Media. DateReleased](../properties/props-system-media-datereleased.md)                       | Data de lançamento original.                                                                                                                                                                                    | LPWStr do VT \_   |
| **\_Duração da mídia do PKEY \_**                                                | [System. Media. Duration](../properties/props-system-media-duration.md)                               | Duração, em unidades de 100 a nanossegundos. Equivalente ao atributo [**de \_ \_ duração de PD MF**](mf-pd-duration-attribute.md) no descritor de apresentação.                                                       | \_UI8 VT      |
| **PKEY \_ Media \_ DVDID**                                                   | [System. Media. DVDID](../properties/props-system-media-dvdid.md)                                     | Identificador de disco de vídeo digital (DVDID).                                                                                                                                                                    | LPWStr do VT \_   |
| **PKEY \_ Media \_ EncodedBy**                                               | [System. Media. EncodedBy](../properties/props-system-media-encodedby.md)                             | Nome da pessoa ou grupo que codificou o conteúdo.                                                                                                                                                     | LPWStr do VT \_   |
| **PKEY \_ Media \_ EncodingSettings**                                        | [System. Media. EncodingSettings](../properties/props-system-media-encodingsettings.md)               | Descrição das configurações usadas para codificar o conteúdo.                                                                                                                                                   | LPWStr do VT \_   |
| **PKEY \_ Media \_ MCDI**                                                    | [System. Media. MCDI](../properties/props-system-media-mcdi.md)                                       | Identificador de CD de música. Esse valor é usado para identificar um CD.                                                                                                                                                 | LPWStr do VT \_   |
| **PKEY \_ Media \_ MetadataContentProvider**                                 | [System. Media. MetadataContentProvider](../properties/props-system-media-metadatacontentprovider.md) | Nome do provedor de conteúdo de metadados. (Por exemplo, os metadados podem ser fornecidos por um serviço comercial.)                                                                                                 | LPWStr do VT \_   |
| **\_Produtor de mídia do PKEY \_**                                                | [System. Media. Producer](../properties/props-system-media-producer.md)                               | Nome do produtor do conteúdo.                                                                                                                                                                      | LPWStr do VT \_   |
| **PKEY \_ Media \_ PromotionUrl**                                            | [System. Media. PromotionUrl](../properties/props-system-media-promotionurl.md)                       | URL de um site que oferece uma promoção relacionada ao conteúdo.                                                                                                                                             | LPWStr do VT \_   |
| **PKEY \_ Media \_ ProviderRating**                                          | [System. Media. ProviderRating](../properties/props-system-media-providerrating.md)                   | Classificação do conteúdo atribuída pelo provedor de conteúdo de metadados.                                                                                                                                       | LPWStr do VT \_   |
| **\_Provedor de mídia PKEY \_**                                           | [System. Media. Providerstyle](../properties/props-system-media-providerstyle.md)                     | Estilo ou gênero do conteúdo conforme atribuído pelo provedor de conteúdo de metadados.                                                                                                                               | LPWStr do VT \_   |
| **\_Publicador de mídia do PKEY \_**                                               | [System. Media. Publisher](../properties/props-system-media-publisher.md)                             | Editor.                                                                                                                                                                                                | LPWStr do VT \_   |
| **Subtítulo de mídia do PKEY \_ \_**                                                | [System. Media. subtítulo](../properties/props-system-media-subtitle.md)                               | Legenda.                                                                                                                                                                                                 | LPWStr do VT \_   |
| **PKEY \_ Media \_ UniqueFileIdentifier**                                    | [System. Media. UniqueFileIdentifier](../properties/props-system-media-uniquefileidentifier.md)       | Uma cadeia de caracteres genérica que pode ser para identificar o arquivo.                                                                                                                                                        | LPWStr do VT \_   |
| **\_Gravador de mídia do PKEY \_**                                                  | [System. Media. Writer](../properties/props-system-media-writer.md)                                   | Escritor.                                                                                                                                                                                                   | LPWStr do VT \_   |
| **\_Ano de mídia do PKEY \_**                                                    | [Sistema. Media. Year](../properties/props-system-media-year.md)                                       | Ano em que o conteúdo foi publicado.                                                                                                                                                                           | \_UI4 VT      |
| **PKEY \_ Music \_ AlbumArtist**                                             | [System. Music. AlbumArtist](../properties/props-system-music-albumartist.md)                         | Artista principal do álbum. Esse atributo pode ser usado para distinguir o artista principal de um álbum de um artista que colaborau em uma determinada faixa.                                            | LPWStr do VT \_   |
| **PKEY \_ Music \_ campos AlbumTitle**                                              | [System. Music. campos AlbumTitle](../properties/props-system-music-albumtitle.md)                           | Título do álbum.                                                                                                                                                                                              | LPWStr do VT \_   |
| **\_Artista de música PKEY \_**                                                  | [System. Music. artista](../properties/props-system-music-artist.md)                                   | Autor.                                                                                                                                                                                                   | LPWStr do VT \_   |
| **PKEY \_ Music \_ BeatsPerMinute**                                          | [System. Music. BeatsPerMinute](../properties/props-system-music-beatsperminute.md)                   | Batidas por minuto.                                                                                                                                                                                         | LPWStr do VT \_   |
| **PKEY \_ Music \_ Composer**                                                | [Sistema. Music. Composer](../properties/props-system-music-composer.md)                               | Composer.                                                                                                                                                                                                 | LPWStr do VT \_   |
| **\_Condutor de música PKEY \_**                                               | [Sistema. Music. condutor](../properties/props-system-music-conductor.md)                             | Conductor.                                                                                                                                                                                                | LPWStr do VT \_   |
| **PKEY \_ Music \_ ContentGroupDescription**                                 | [System. Music. ContentGroupDescription](../properties/props-system-music-contentgroupdescription.md) | Descrição do grupo de conteúdo (por exemplo, conjunto ou série em caixa).                                                                                                                                      | LPWStr do VT \_   |
| **\_Gênero de música PKEY \_**                                                   | [System. Music. Gênero](../properties/props-system-music-genre.md)                                     | \.                                                                                                                                                                                                    | LPWStr do VT \_   |
| **PKEY \_ Music \_ InitialKey**                                              | [System.Music.InitialKey](../properties/props-system-music-initialkey.md)                           | A chave inicial da música.                                                                                                                                                                             | LPWStr do VT \_   |
| **Iscompilação de \_ música PKEY \_**                                           | [System. Music. iscompilation](../properties/props-system-music-iscompilation.md)                     | Indica se o arquivo de música faz parte de uma compilação.                                                                                                                                                | BOOL do VT \_     |
| **PKEY \_ músicas de música \_**                                                  | [Sistema. Music. letras](../properties/props-system-music-lyrics.md)                                   | Letra.                                                                                                                                                                                                   | LPWStr do VT \_   |
| **PKEY \_ música de \_ humor**                                                    | [System. Music. humor](../properties/props-system-music-mood.md)                                       | Espírito.                                                                                                                                                                                                     | LPWStr do VT \_   |
| **PKEY \_ Music \_ PartOfSet**                                               | [System. Music. PartOfSet](../properties/props-system-music-partofset.md)                             | O número da peça e o número total de partes no conjunto ao qual o arquivo pertence, separados por uma barra.                                                                                                 | LPWStr do VT \_   |
| **PKEY \_ o \_ período de música**                                                  | [Sistema. Music. period](../properties/props-system-music-period.md)                                   | Período.                                                                                                                                                                                                   | LPWStr do VT \_   |
| **PKEY \_ Music \_ TrackNumber**                                             | [System. Music. TrackNumber](../properties/props-system-music-tracknumber.md)                         | Número de faixa.                                                                                                                                                                                             | \_UI4 VT      |
| **PKEY \_ ParentalRating**                                                 | [System. ParentalRating](../properties/props-system-parentalrating.md)                               | Classificação de pais.                                                                                                                                                                                          | LPWStr do VT \_   |
| **PKEY \_ ParentalRatingReason**                                           | [System. ParentalRatingReason](../properties/props-system-parentalratingreason.md)                   | Motivos para a classificação de pais atribuída.                                                                                                                                                                 | LPWStr do VT \_   |
| **Classificação de PKEY \_**                                                         | [System. rating](../properties/props-system-rating.md)                                               | Classificação do usuário.                                                                                                                                                                                              | \_UI4 VT      |
| **PKEY \_ ThumbnailStream**                                                | [System. ThumbnailStream](../properties/props-system-thumbnailstream.md)                             | Imagem em miniatura.                                                                                                                                                                                          | \_fluxo VT   |
| **Título do PKEY \_**                                                          | [System.Title](../properties/props-system-title.md)                                                 | Título.                                                                                                                                                                                                    | LPWStr do VT \_   |
| **\_Compactação de vídeo PKEY \_**                                             | [System. vídeo. Compression](../properties/props-system-video-compression.md)                         | Subtipo de vídeo [**( \_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)) expresso como uma cadeia de caracteres.                                                                                                                 | LPWStr do VT \_   |
| **\_Diretor de vídeo PKEY \_**                                                | [System. vídeo. director](../properties/props-system-video-director.md)                               | Pasta.                                                                                                                                                                                                 | LPWStr do VT \_   |
| **PKEY \_ vídeo \_ EncodingBitrate**                                         | [System. vídeo. EncodingBitrate](../properties/props-system-video-encodingbitrate.md)                 | Taxa média de bits de vídeo, em bits por segundo.                                                                                                                                                               | \_UI4 VT      |
| **PKEY de \_ vídeo \_ FOURCC**                                                  | [System. video. FourCC](../properties/props-system-video-fourcc.md)                                   | O **FOURCC** do formato de codificação de vídeo. Aplica-se somente se o subtipo de vídeo puder ser expresso como um valor **FOURCC** .                                                                                    | \_UI4 VT      |
| **PKEY \_ vídeo \_ FrameHeight**                                             | [System. vídeo. FrameHeight](../properties/props-system-video-frameheight.md)                         | Altura do quadro do vídeo.                                                                                                                                                                                       | \_UI4 VT      |
| **Taxa de quadros de \_ vídeo PKEY \_**                                               | [System. vídeo. taxa de quadros](../properties/props-system-video-framerate.md)                             | Taxa de quadros de vídeo, expressa como quadros por segundo × 1000.                                                                                                                                                  | \_UI4 VT      |
| **PKEY \_ vídeo \_ FrameWidth**                                              | [System. vídeo. FrameWidth](../properties/props-system-video-framewidth.md)                           | Largura do quadro do vídeo.                                                                                                                                                                                        | \_UI4 VT      |
| **PKEY \_ vídeo \_ HorizontalAspectRatio**                                   | [System. vídeo. HorizontalAspectRatio](../properties/props-system-video-horizontalaspectratio.md)     | O componente horizontal da taxa de proporção de pixel. (Equivalente ao numerador do atributo [**de \_ \_ taxa de \_ proporção \_ MF MT pixel**](mf-mt-pixel-aspect-ratio-attribute.md) no tipo de mídia.)          | \_UI4 VT      |
| **Isestéreo de \_ vídeo PKEY \_**                                                | [System. vídeo. isestéreo](/previous-versions//mt744507(v=vs.85))                                     | Indica se o fluxo de vídeo contém conteúdo de vídeo estéreo.                                                                                                                                         | BOOL do VT \_     |
| **PKEY \_ vídeo \_ StreamNumber**                                            | [System. vídeo. StreamNumber](../properties/props-system-video-streamnumber.md)                       | Identificador do fluxo de vídeo.                                                                                                                                                                           | \_UI4 VT      |
| **PKEY \_ vídeo \_ TotalBitrate**                                            | [System. vídeo. TotalBitrate](../properties/props-system-video-totalbitrate.md)                       | Taxa total de dados para todos os fluxos de áudio e vídeo em bits por segundo. (Aplica-se somente a arquivos com pelo menos um fluxo de vídeo.)                                                                              | \_UI4 VT      |
| **PKEY \_ vídeo \_ VerticalAspectRatio**                                     | [System. vídeo. VerticalAspectRatio](../properties/props-system-video-verticalaspectratio.md)         | O componente vertical da taxa de proporção de pixel. (Equivalente ao denominador do atributo [**de \_ \_ taxa de \_ proporção \_ MF MT pixel**](mf-mt-pixel-aspect-ratio-attribute.md) no tipo de mídia.)          | \_UI4 VT      |



 

## <a name="media-sharing-properties"></a>Propriedades de compartilhamento de mídia

Para tornar um arquivo de mídia compatível com o recurso de compartilhamento de mídia, o manipulador de propriedades deve expor as propriedades de metadados a seguir. Essas propriedades permitem que o serviço de compartilhamento de mídia ofereça as opções apropriadas para transcodificar o conteúdo em diferentes formatos ou taxas de bits.

-   [\_ID do \_ perfil de DLNA do conteúdo do MFPKEY \_ \_](mfpkey-content-dlna-profile-id.md)
-   **PKEY de \_ áudio \_ ChannelCount**
-   **PKEY de \_ áudio \_ EncodingBitrate**
-   **\_Formato de áudio PKEY \_**
-   **PKEY \_ \_Amostra de áudio** (opcional)
-   **PKEY \_ \_Amostras de áudio** (opcional)
-   **PKEY \_ \_Protegido por DRM** (necessário para conteúdo de DRM)
-   **\_Duração da mídia do PKEY \_**
-   **\_Compactação de vídeo PKEY \_**
-   **PKEY \_ vídeo \_ EncodingBitrate**
-   **PKEY de \_ vídeo \_ FOURCC**
-   **PKEY \_ vídeo \_ FrameHeight**
-   **PKEY \_ \_Taxa de quadros de vídeo** (opcional)
-   **PKEY \_ vídeo \_ FrameWidth**
-   **PKEY \_ vídeo \_ TotalBitrate**

A **propriedade \_ \_ Isprotegida do PKEY DRM** será necessária se o conteúdo estiver protegido usando DRM. Caso contrário, essa propriedade é opcional.

As propriedades de PKEY de **\_ áudio PKEY \_**, **\_ \_ amostras** de áudio e **PKEY de \_ taxa de \_ quadros de vídeo** são opcionais. O serviço de compartilhamento de mídia irá expô-los se estiverem disponíveis.

As propriedades no **\_ grupo PKEY Audio \_ \* *_ aplicam-se somente a arquivos com um fluxo de áudio, e as propriedades no grupo de* \_ vídeos \_ \* _ PKEY** aplicam-se somente a arquivos com um fluxo de vídeo.

## <a name="windows-media-format-sdk-mappings"></a>Mapeamentos do Windows Media Format SDK

A fonte de mídia ASF mapeia as seguintes chaves de propriedade para atributos de cabeçalho ASF. Em alguns casos, os tipos de dados diferem entre a propriedade Shell e o atributo Format SDK.



| PROPERTYKEY                              | Formatar atributo do SDK                                                  |
|------------------------------------------|-----------------------------------------------------------------------|
| **PKEY de \_ áudio \_ IsVariableBitRate**       | [**IsVBR**](../wmformat/isvbr.md)                                           |
| **\_Picovalue de áudio PKEY \_**               | [**Picovalue**](../wmformat/peakvalue.md)                                   |
| **Autor do PKEY \_**                         | [**Autor**](../wmformat/author.md)                                         |
| **Comentário de PKEY \_**                        | [**Descrição**](../wmformat/description.md)                               |
| **\_Direitos autorais do PKEY**                      | [**Direitos autorais**](../wmformat/copyright.md)                                   |
| **PKEY \_ DRM \ \_ protegido**               | [**É \_ protegido**](../wmformat/is-protected.md)                            |
| **\_Palavras-chave PKEY**                       | [**WM/categoria**](../wmformat/wm-category.md)                               |
| **\_Linguagem PKEY**                       | [**WM/linguagem**](../wmformat/wm-language.md)                               |
| **PKEY \_ Media \_ AuthorUrl**               | [**WM/AuthorURL**](../wmformat/wm-authorurl.md)                             |
| **PKEY \_ Media \_ AverageLevel**            | [**AverageLevel**](../wmformat/averagelevel.md)                             |
| **PKEY \_ Media \_ ClassPrimaryID**          | [**WM/MediaClassPrimaryID**](../wmformat/wm-mediaprimaryid.md)              |
| **PKEY \_ Media \_ ClassSecondaryID**        | [**WM/MediaClassSecondaryID**](../wmformat/wm-mediasecondaryid.md)          |
| **PKEY \_ Media \_ CollectionGroupID**       | [**WM/WMCollectionGroupID**](../wmformat/wm-wmcollectiongroupid.md)         |
| **\_Conjunto de \_ coletas de mídia PKEY**            | [**WM/WMCollectionID**](../wmformat/wm-wmcollectionid.md)                   |
| **PKEY \_ Media \_ ContentDistributor**      | [**WM/ContentDistributor**](../wmformat/wm-contentdistributor.md)           |
| **\_ContentId de mídia PKEY \_**               | [**WM/WMContentID**](../wmformat/wm-wmcontentid.md)                         |
| **PKEY \_ Media \_ DateEncoded**             | [**WM/Codificaçãotime**](../wmformat/wm-encodingtime.md)                       |
| **PKEY \_ Media \_ DateReleased**            | [**WM/OriginalReleaseTime**](../wmformat/wm-originalreleasetime.md)         |
| **PKEY \_ Media \_ DVDID**                   | [**WM/DVDID**](../wmformat/wm-dvdid.md)                                     |
| **PKEY \_ Media \_ EncodedBy**               | [**WM/EncodedBy**](../wmformat/wm-encodedby.md)                             |
| **PKEY \_ Media \_ EncodingSettings**        | [**WM/EncodingSettings**](../wmformat/wm-encodingsettings.md)               |
| **PKEY \_ Media \_ MCDI**                    | [**WM/MCDI**](../wmformat/wm-mcdi.md)                                       |
| **PKEY \_ Media \_ MetadataContentProvider** | [**WM/provedor**](../wmformat/wm-provider.md)                               |
| **\_Produtor de mídia do PKEY \_**                | [**WM/produtor**](../wmformat/wm-producer.md)                               |
| **PKEY \_ Media \_ PromotionUrl**            | [**WM/PromotionURL**](../wmformat/wm-promotionurl.md)                       |
| **PKEY \_ Media \_ ProviderRating**          | [**WM/ProviderRating**](../wmformat/wm-providerrating.md)                   |
| **\_Provedor de mídia PKEY \_**           | [**WM/Provedorstyle**](../wmformat/wm-providerstyle.md)                     |
| **\_Publicador de mídia do PKEY \_**               | [**WM/Publicador**](../wmformat/wm-publisher.md)                             |
| **Subtítulo de mídia do PKEY \_ \_**                | [**WM/SubTitleDescription**](../wmformat/wm-subtitledescription.md)         |
| **PKEY \_ Media \_ UniqueFileIdentifier**    | [**WM/UniqueFileIdentifier**](../wmformat/wm-uniquefileidentifier.md)       |
| **\_Gravador de mídia do PKEY \_**                  | [**WM/gravador**](../wmformat/wm-writer.md)                                   |
| **\_Ano de mídia do PKEY \_**                    | [**WM/ano**](../wmformat/wm-year.md)                                       |
| **PKEY \_ Music \_ AlbumArtist**             | [**WM/AlbumArtist**](../wmformat/wm-albumartist.md)                         |
| **PKEY \_ Music \_ campos AlbumTitle**              | [**WM/campos AlbumTitle**](../wmformat/wm-albumtitle.md)                           |
| **\_Artista de música PKEY \_**                  | [**Autor**](../wmformat/author.md)                                         |
| **PKEY \_ Music \_ BeatsPerMinute**          | [**WM/BeatsPerMinute**](../wmformat/wm-beatsperminute.md)                   |
| **PKEY \_ Music \_ Composer**                | [**WM/Composer**](../wmformat/wm-composer.md)                               |
| **\_Condutor de música PKEY \_**               | [**WM/condutor**](../wmformat/wm-conductor.md)                             |
| **PKEY \_ Music \_ ContentGroupDescription** | [**WM/ContentGroupDescription**](../wmformat/wm-contentgroupdescription.md) |
| **\_Gênero de música PKEY \_**                   | [**WM/gênero**](../wmformat/wm-genre.md)                                     |
| **PKEY \_ Music \_ InitialKey**              | [**WM/InitialKey**](../wmformat/wm-initialkey.md)                           |
| **Iscompilação de \_ música PKEY \_**           | **WM/iscompilation**                                                  |
| **PKEY \_ músicas de música \_**                  | [**WM/letras de música**](../wmformat/wm-lyrics.md)                                   |
| **PKEY \_ música de \_ humor**                    | [**WM/humor**](../wmformat/wm-mood.md)                                       |
| **PKEY \_ Music \_ PartOfSet**               | [**WM/PartOfSet**](../wmformat/wm-partofset.md)                             |
| **PKEY \_ o \_ período de música**                  | [**WM/período**](../wmformat/wm-period.md)                                   |
| **PKEY \_ Music \_ TrackNumber**             | [**WM/TrackNumber**](../wmformat/wm-tracknumber.md)                         |
| **PKEY \_ ParentalRating**                 | [**WM/ParentalRating**](../wmformat/wm-parentalrating.md)                   |
| **PKEY \_ ParentalRatingReason**           | [**WM/ParentalRatingReason**](../wmformat/wm-parentalratingreason.md)       |
| **Classificação de PKEY \_**                         | [**WM/SharedUserRating**](../wmformat/wm-shareduserrating.md)               |
| **PKEY \_ ThumbnailStream**                | [**WM/imagem**](../wmformat/wmpicture.md)                       |
| **Título do PKEY \_**                          | [**Título**](../wmformat/title.md)                                           |
| **\_Diretor de vídeo PKEY \_**                | [**WM/diretor**](../wmformat/wm-director.md)                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Metadados de mídia](media-metadata.md)
</dt> <dt>

[Provedores de metadados do Shell](shell-metadata-providers.md)
</dt> </dl>

 

 
