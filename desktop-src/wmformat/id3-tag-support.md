---
title: Suporte à marca ID3
description: Suporte à marca ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- Windows SDK de Formato de Mídia, atributos
- ASF (Advanced Systems Format), attributes
- ASF (Formato de Sistemas Avançados), atributos
- atributos, marcas ID3
- Marcas ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fd65ffadb952e9370af609e336c08fc07c9b96f50d09d95c78492bef2163db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703021"
---
# <a name="id3-tag-support"></a>Suporte à marca ID3

A tabela a seguir lista todos os atributos que correspondem às marcas ID3. Se você quiser usar as marcas ID3 como atributos em vez de usar os nomes de atributo padrão, adicione o prefixo "ID3/" ao nome da marca. Por exemplo, "ID3/TPE2" é equivalente a **Author**.



| Atributo                      | ID3v1.x | ID3v2.2 | ID3v2.3/v2.4 |
|--------------------------------|---------|---------|--------------|
| **Author**                     | Artista  | TP1     | TPE1         |
| **Direitos autorais**                  |         | Tcr     | TCOP         |
| **CopyrightURL**               |         | Wcp     | WCOP         |
| **Descrição**                | Comentário | COM     | COMM         |
| **Duration**                   |         | Tle     | TLEN         |
| **FileSize**                   |         |         | TSIZ         |
| **Título**                      | Título   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/AlbumTitle**              | Álbum   | TAL     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/Binário**                  |         | Geo     | GEOB         |
| **WM/Comments**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/Wm/Wm**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | Dez     | TENC         |
| **WM/EncodingSettings**        |         | Tss     | TSSE         |
| **WM/EncodingTime**            |         |         | TDEN         |
| **WM/GenreID**                 | GenreID | TCO     | TCON         |
| **WM/InitialKey**              |         |         | Tkey         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/Language**                |         | Tla     | TLAN         |
| **\_WM/Synchronizado**    |         | Slt     | Sylt         |
| **WM/MCDI**                    |         |         | MCDI         |
| **WM/ModifiedBy**              |         |         | TPE4         |
| **WM/humor**                    |         |         | TMOO         |
| **WM/OriginalAlbumTitle**      |         | Transp     | TOAL         |
| **WM/OriginalArtist**          |         | AUTORIDADES     | PARTE superior         |
| **WM/OriginalFilename**        |         | TOF     | TOFN         |
| **WM/OriginalLyricist**        |         | A     | TOLY         |
| **WM/OriginalReleaseYear**     |         | TOR     | TORY         |
| **WM/PartOfSet**               |         | TPA     | TPOS         |
| **WM/imagem**                 |         | IMG     | APIC         |
| **WM/PlaylistDelay**           |         |         | TDLY         |
| **WM/Publisher**               |         | TPB     | TPUB         |
| **WM/RadioStationName**        |         | TRN     | TRSN         |
| **WM/RadioStationOwner**       |         | TRO     | TRSO         |
| **WM/subtítulo**             |         |         | TSST         |
| **WM/subtítulo**                |         | TT3     | TIT3         |
| **WM/texto**                    |         | TXX     | TXXX         |
| **WM/TitleSortOrder**          |         |         | TSOT         |
| **WM/TrackNumber**             | Rastrear   | TRK     | TRCK         |
| **WM/UniqueFileIdentifier**    |         | UFI     | UFID         |
| **WM/UserWebURL**              |         | WXX     | WXXX         |
| **WM/gravador**                  |         | TXT     | TEXT         |
| **WM/ano**                    | Year    | TYE     | TYER         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 




