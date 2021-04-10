---
title: Redirecionamento
description: Redirecionamento
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Listas de reprodução do metarquivo do Windows Media, redirecionamento
- listas de reprodução, redirecionamento
- listas de reprodução de metarquivo, redirecionamento
- Windows Media Player, redirecionamento
- redirecionamento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291832"
---
# <a name="redirection"></a>Redirecionamento

A lista de reprodução redirecionará o navegador para o Windows Media Player para reproduzir o fluxo de mídia designado ou o arquivo de mídia. A lista de reprodução de metarquivo mais básica contém apenas o Uniform Resource Locator (URL) de um arquivo de mídia.

Para criar uma lista de reprodução de metarquivo básico, abra seu editor de texto favorito, como o bloco de notas da Microsoft e digite o código de exemplo a seguir.


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



Substitua um caminho válido para o arquivo de mídia do Windows usando a sintaxe na tabela a seguir.



| Fonte de conteúdo                                                                                 | Syntax                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| O conteúdo é um arquivo em um servidor do Windows Media                                                       | mms://ServerName/Path/FileName.wma        |
| O conteúdo é um multicast de difusão que é acessado de uma estação de mídia do Windows                    | https://WebServerName/Stations/kxyz.nsc    |
| O conteúdo é uma difusão unicast que é acessada de um ponto de publicação em um Windows Media Server | mms://ServerName/PublishingPointAlias     |
| O conteúdo é um arquivo em um servidor Web                                                                 | https://WebServerName/Path/Filename.wma    |
| O conteúdo é um arquivo em um disco rígido local                                                            | file://c: \\ caminho \\ filename. WMA             |
| O conteúdo é um arquivo em um compartilhamento de rede                                                              | file:// \\ \\ ServerName \\ caminho \\ nome_do_arquivo. WMA |
| O conteúdo é um arquivo em um servidor do Windows Media                                                       | mms://ServerName/Path/FileName.wmv        |



 

Salve o arquivo que você criou com um nome de arquivo e extensão, conforme descrito em [extensões de nome de arquivo](file-name-extensions.md). Clique duas vezes no Windows Explorer. O Windows Media Player deve abrir e começar a transmitir o conteúdo. Você pode salvar o arquivo em seu servidor Web, juntamente com suas páginas da Web, e vinculá-lo a um elemento **href** ou inseri-lo em uma página da Web usando a marca de **objeto** do Windows Media Player.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




