---
title: Lista de Atributos
description: Lista de Atributos
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, lista de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499048"
---
# <a name="attribute-list"></a>Lista de Atributos

Os atributos predefinidos incluídos neste SDK são apresentados em ordem alfabética na tabela a seguir. Cada atributo tem um nome, um identificador global e um tipo de dados, conforme definido pelo membro apropriado da enumeração [**de \_ \_ DataType WMT attr**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) . Alguns atributos não usam um tipo de dados simples ou são formatados de acordo com uma estrutura. As entradas para esses atributos listam um nome de estrutura na coluna tipo de dados com o tipo de dados usado para definir o valor entre parênteses.

> [!Note]  
> Consulte [lista de atributos DRM](drm-attribute-list.md) para obter uma tabela de todos os atributos relacionados ao DRM.

 

Ao programar com esses atributos, você deve usar o identificador global em vez de usar o nome como um literal de cadeia de caracteres. Usando o identificador global, quaisquer erros tipográficos resultarão em um erro no momento da compilação.



| Nome do atributo                                                                       | Identificador global                             | Tipo de dados                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **WMT \_ tipo \_ binário**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **WMT \_ tipo \_ DWORD**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **WMT \_ tipo \_ DWORD**                                 |
| [**Autor**](author.md)                                                             | g \_ wszWMAuthor                                | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **WMT \_ tipo \_ DWORD**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **WMT \_ tipo \_ binário**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **WMT \_ tipo \_ DWORD**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**720p**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **WMT \_ tipo \_ DWORD**                                 |
| [**Transmissão**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **WMT \_ tipo \_ bool**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **WMT \_ tipo \_ DWORD**                                 |
| [**Pode \_ pular \_ para trás**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **WMT \_ tipo \_ bool**                                  |
| [**Pode \_ pular para \_ frente**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **WMT \_ tipo \_ bool**                                  |
| [**Direitos autorais**](copyright.md)                                                       | g \_ wszWMCopyright                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**Descrição**](description.md)                                                   | g \_ wszWMDescription                           | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_ContentId DRM**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentId                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_ContentDistributor DRMHEADER \_ DRM**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_ContentId do DRM DRMHeader \_**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentId             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_IndividualizedVersion DRMHEADER \_ DRM**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_Keyid DRMHEADER \_ DRM**](drm-drmheader-keyid.md)                                 | \_keyid g wszWMDRM \_ DRMHeader \_                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LicenseAcqURL DRMHEADER \_ DRM**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_SubscriptionContentID DRMHEADER \_ DRM**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_DRMHEADER DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_Keyid DRM**](drm-keyid.md)                                                      | \_keyid g wszWMDRM \_                            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_Licenseid DRM**](drm-licenseid.md)                                              | \_licença de wszWMDRM g \_                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_SourceID DRM**](drm-sourceid.md)                                                | \_fonte de wszWMDRM g \_                         | **WMT \_ tipo \_ DWORD**                                 |
| [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**Duration**](duration.md)                                                         | g \_ wszWMDuration                              | **WMT \_ tipo \_ QWORD**                                 |
| [**Tamanho**](filesize.md)                                                         | g \_ wszWMFileSize                              | **WMT \_ tipo \_ QWORD**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **WMT \_ tipo \_ bool**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **WMT \_ tipo \_ bool**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **WMT \_ tipo \_ bool**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **WMT \_ tipo \_ bool**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **WMT \_ tipo \_ bool**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **WMT \_ tipo \_ bool**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **WMT \_ tipo \_ bool**                                  |
| [**É \_ protegido**](is-protected.md)                                                | g \_ wszWMProtected                             | **WMT \_ tipo \_ bool**                                  |
| [**É \_ confiável**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **WMT \_ tipo \_ bool**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszISAN                                    | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **WMT \_ tipo \_ bool**                                  |
| [**\_Endereço NSC**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**Descrição de NSC \_**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_Email NSC**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**Nome de NSC \_**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**\_Telefone NSC**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **WMT \_ tipo \_ QWORD**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**Picovalue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **WMT \_ tipo \_ DWORD**                                 |
| [**Classificação**](rating.md)                                                             | g \_ wszWMRating                                | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**Busca**](seekable.md)                                                         | g \_ wszWMSeekable                              | **WMT \_ tipo \_ bool**                                  |
| [**Nome da assinatura \_**](signature-name.md)                                            | nome do g \_ wszWMSignature \_                       | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**Stridable**](stridable.md)                                                       | g \_ wszWMStridable                             | **WMT \_ tipo \_ bool**                                  |
| [**Título**](title.md)                                                               | g \_ wszWMTitle                                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMAlbumArtist                           | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMAlbumCoverURL                         | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/campos AlbumTitle**](wm-albumtitle.md)                                               | g \_ wszWMAlbumTitle                            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **WMT \_ tipo \_ QWORD**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **WMT \_ tipo \_ QWORD**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/categoria**](wm-category.md)                                                   | g \_ wszWMCategory                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/codec**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Composer**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/condutor**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ \_formato de armazenamento** (**WMT \_ tipo \_ Binary**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/diretor**](wm-director.md)                                                   | g \_ wszWMDirector                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Codificaçãotime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**WMT \_ tipo \_ QWORD**)                  |
| [**WM/gênero**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Gêneroid**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/linguagem**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/letras de música**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/letras de música \_ sincronizadas**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ sincronizadas                  | **WM \_ letras de \_ música sincronizadas** (**\_ tipo \_ binário WMT**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **WMT \_ tipo \_ binário**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **\_GUID do tipo WMT \_**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **\_GUID do tipo WMT \_**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **WMT \_ tipo \_ bool**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/humor**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalAlbumTitle                    | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/período**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/imagem**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_ PICTURE** (**\_ tipo \_ binário WMT**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/produtor**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/provedor**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Provedorstyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Publicador**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | g \_ wszWMRadioStationName                      | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWMRadioStationOwner                     | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_ \_ \_ informações de tipo de fluxo** (**WMT \_ tipo \_ Binary**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/subtítulo**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/texto**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_ \_texto do usuário** (**\_ tipo WMT \_ Binary**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ToolVersion**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/Track**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_ \_ \_ URL da Web do usuário** (**\_ tipo WMT \_ Binary**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **WMT \_ tipo \_ bool**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **WMT \_ tipo \_ DWORD**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **\_GUID do tipo WMT \_**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **\_GUID do tipo WMT \_**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **\_GUID do tipo WMT \_**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/gravador**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **Cadeia de caracteres do \_ tipo WMT \_**                                |
| [**WM/ano**](wm-year.md)                                                           | g \_ wszWMYear                                  | **Cadeia de caracteres do \_ tipo WMT \_**                                |



 

## <a name="remarks"></a>Comentários

As constantes a seguir são definidas com os atributos. Cada uma indica o número de um tipo específico de atributo. Você não precisa usar esses valores para nada em seus aplicativos.



| Constante                 | Valor |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 