---
title: Suporte a marcas ID3
description: Suporte a marcas ID3
ms.assetid: 57119b88-5901-4bea-abf6-a67fe71afd1b
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, marcas ID3
- Marcas ID3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3dd91119aedf2983e654b4925231b8fd9e4b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005939"
---
# <a name="id3-tag-support"></a>Suporte a marcas ID3

A tabela a seguir lista todos os atributos que correspondem às marcas ID3. Se você quiser usar as marcas ID3 como atributos em vez de usar os nomes de atributo padrão, adicione o prefixo "ID3/" ao nome da marca. Por exemplo, "ID3/TPE2" é equivalente a **Author**.



| Atributo                      | ID3v1. x | ID3v 2.2 | ID3v 2.3/v 2.4 |
|--------------------------------|---------|---------|--------------|
| **Autor**                     | Autor  | TP1     | TPE1         |
| **Direitos autorais**                  |         | TCR     | TCOP         |
| **CopyrightURL**               |         | WCP     | WCOP         |
| **Descrição**                | Comentário | COM     | COMM         |
| **Duration**                   |         | TLE     | TLEN         |
| **Tamanho**                   |         |         | TSIZ         |
| **Título**                      | Título   | TT2     | TIT2         |
| **WM/AlbumArtist**             |         | TP2     | TPE2         |
| **WM/AlbumSortOrder**          |         |         | TSOA         |
| **WM/campos AlbumTitle**              | Álbuns   | TAL     | TALB         |
| **WM/ArtistSortOrder**         |         |         | TSOP         |
| **WM/AudioFileURL**            |         | WAF     | WOAF         |
| **WM/AudioSourceURL**          |         | WAS     | WOAS         |
| **WM/AuthorURL**               |         | WAR     | WOAR         |
| **WM/BeatsPerMinute**          |         |         | TBPM         |
| **WM/binário**                  |         | GRAFICAMENTE     | GEOB         |
| **WM/comentários**                |         | COM     | COMM         |
| **WM/Composer**                |         | TCM     | TCOM         |
| **WM/condutor**               |         | TP3     | TPE3         |
| **WM/ContentGroupDescription** |         | TT1     | TIT1         |
| **WM/EncodedBy**               |         | DEZ     | TENC         |
| **WM/EncodingSettings**        |         | TSS     | TSSE         |
| **WM/Codificaçãotime**            |         |         | TDEN         |
| **WM/Gêneroid**                 | Gêneroid | TCO     | TCON         |
| **WM/InitialKey**              |         |         | TKEY         |
| **WM/ISRC**                    |         |         | TSRC         |
| **WM/linguagem**                |         | TLA     | TLAN         |
| **WM/letras de música \_ sincronizadas**    |         | SLT     | SYLT         |
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
| **WM/Publicador**               |         | TPB     | TPUB         |
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

 

 




