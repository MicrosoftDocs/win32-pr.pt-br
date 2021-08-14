---
title: Diretrizes de extensão de metarquivo
description: Diretrizes de extensão de metarquivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Metaarquivos de mídia, extensões
- Windows Metaarquivos de mídia, extensões de nome de arquivo
- metaarquivos, extensões
- metaarquivos, extensões de nome de arquivo
- Windows Mídia, metaarquivos
- extensões de nome de arquivo para os metaarquivos de mídia Windows
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aaa31f1364271b1b968244494586ba5006e7c292ca2d9a207cdd1c758b5e432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836963"
---
# <a name="metafile-extension-guidelines"></a>Diretrizes de extensão de metarquivo

Uma extensão de nome de arquivo fornece um fornecedor de software independente (ISV) com informações sobre os requisitos de renderização de um aplicativo que usa a extensão e permite que os autores de conteúdo direcionem tipos gerais de players.

Windows extensões de nome de metarquivo de mídia são usadas para identificar o formato dos arquivos de mídia Windows que um metarquivo faz referência. Windows Os metaarquivos de mídia com extensões. Wax,. wvx ou. asx fazem referência a arquivos com as extensões. WMA,. wmv e. ASF, respectivamente. Todos os metaarquivos, independentemente da extensão de nome de arquivo usada, têm a marca de elemento **ASX** no início do arquivo com o atributo **version** especificado.

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

[**Windows Guia de metarquivo de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




