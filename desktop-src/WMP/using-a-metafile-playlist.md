---
title: Usando uma lista de reprodução de metarquivo
description: Usando uma lista de reprodução de metarquivo
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Playlists do metarquivo do Windows Media, usando
- listas de reprodução de metarquivo, usando
- listas de reprodução, usando
- Listas de reprodução do metarquivo do Windows Media, sobre
- listas de reprodução de metarquivo, sobre
- listas de reprodução, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635685"
---
# <a name="using-a-metafile-playlist"></a>Usando uma lista de reprodução de metarquivo

Como não é possível vincular diretamente de uma página da Web a um servidor de mídia de streaming, você usa listas de reprodução de metarquivo. As listas de reprodução do metarquivo contêm as informações necessárias para o Windows Media Player e são armazenadas em um servidor Web. Em seguida, você pode vincular do documento da Web a uma lista de reprodução de metarquivo. Quando uma lista de reprodução de metarquivo é aberta, o controla as transferências para o Windows Media Player, que processa o arquivo, conecta-se ao servidor de streaming de mídia e reproduz o conteúdo especificado.

O navegador primeiro baixa a lista de reprodução do metarquivo para o diretório de cache do usuário. Como a lista de reprodução do metarquivo é pequena, essa é uma etapa muito rápida. Em seguida, o computador do usuário encontra em sua tabela associações de arquivo a associação da lista de reprodução do metarquivo ao Windows Media Player. O Windows Media Player abre e interpreta os scripts na lista de reprodução do metarquivo, que contém, entre outras coisas, a URL do conteúdo de streaming. O Windows Media Player usa a URL para localizar o conteúdo e iniciar o fluxo. A lista de reprodução de metarquivos controla a experiência de streaming.

Como as listas de reprodução de metarquivo funcionam por meio de um aplicativo auxiliar associado ao tipo ASXMIME (Application/mplayer2 ou video/x-ms-asf), elas são compatíveis com qualquer navegador que dê suporte a aplicativos auxiliares. Os exemplos mostrados neste documento funcionarão com o Microsoft Internet Explorer 4,0 e posterior e com o Netscape Navigator 4,0 e posterior nas plataformas Microsoft Win32® e Apple Macintosh. Em todos os exemplos, você precisará ter certeza de que todos os arquivos de mídia digital referenciados têm caminhos e nomes de arquivos válidos para o seu ambiente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Visão geral dos metaarquivos do Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




