---
title: Diretrizes de extensão de metarquivo
description: Diretrizes de extensão de metarquivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Metaarquivos do Windows Media, extensões
- Metaarquivos do Windows Media, extensões de nome de arquivo
- metaarquivos, extensões
- metaarquivos, extensões de nome de arquivo
- Windows Media, metaarquivos
- extensões de nome de arquivo para os metaarquivos do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006092"
---
# <a name="metafile-extension-guidelines"></a>Diretrizes de extensão de metarquivo

Uma extensão de nome de arquivo fornece um fornecedor de software independente (ISV) com informações sobre os requisitos de renderização de um aplicativo que usa a extensão e permite que os autores de conteúdo direcionem tipos gerais de players.

Extensões de nome de metarquivo do Windows Media são usadas para identificar o formato dos arquivos de mídia do Windows que um metarquivo faz referência. Os metaarquivos do Windows Media com extensões. Wax,. wvx ou. asx fazem referência a arquivos com as extensões. WMA,. wmv e. ASF, respectivamente. Todos os metaarquivos, independentemente da extensão de nome de arquivo usada, têm a marca de elemento **ASX** no início do arquivo com o atributo **version** especificado.

A tabela a seguir mostra os tipos de arquivo de mídia referenciados por cada tipo de extensão de nome de arquivo de metarquivo. As colunas listam extensões de nome de arquivo de mídia, as linhas listam extensões de nome de metarquivo. Um X em uma coluna indica um tipo de arquivo de mídia que pode ser referenciado por uma extensão de nome de arquivo de metarquivo específica.



| Extensão | .asf | .wma | .wmv |
|-----------|------|------|------|
| .wvx      | X    | X    | X    |
| . Wax      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de nome de arquivo**](file-name-extensions.md)
</dt> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




