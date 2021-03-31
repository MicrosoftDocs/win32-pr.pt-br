---
title: Suporte para vários idiomas
description: Suporte para vários idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Playlists do metarquivo do Windows Media, suporte para vários idiomas
- listas de reprodução de metarquivo, suporte para vários idiomas
- listas de reprodução, suporte para vários idiomas
- Playlists do metarquivo do Windows Media, suporte a vários idiomas
- playlists de metarquivo, suporte a vários idiomas
- playlists, suporte a vários idiomas
- Playlists do metarquivo do Windows Media, suporte a idiomas
- playlists de metarquivo, suporte a idiomas
- playlists, suporte a idiomas
- suporte para vários idiomas
- suporte a vários idiomas.
- suporte de idiomas
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005999"
---
# <a name="support-for-multiple-languages"></a>Suporte para vários idiomas

O Windows Media Player 9 Series ou posterior dá suporte a arquivos de mídia do Windows Media criados usando o conjunto de caracteres Unicode. Isso permite que você inclua metadados multilíngües na sua lista de reprodução de metarquivo. As regras a seguir regem o uso de metadados multilíngües em metaarquivos do Windows Media:

-   Os caracteres devem ser codificados usando o esquema de codificação UTF-8.
-   A lista de reprodução de metarquivo deve incluir o seguinte **parâmetro** no nível de playlist:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   Somente o Windows Media Player 9 Series ou posterior dá suporte a essa funcionalidade.
-   Se a lista de reprodução do metarquivo não for salva com codificação UTF-8 e o elemento **param** correto, ela será analisada usando a página de código padrão de localidade do sistema do computador do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Visão geral dos metaarquivos do Windows Media**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




