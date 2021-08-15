---
title: Suporte para vários idiomas
description: Suporte para vários idiomas
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Playlists de metarquivo de mídia, suporte para vários idiomas
- listas de reprodução de metarquivo, suporte para vários idiomas
- listas de reprodução, suporte para vários idiomas
- Windows Playlists de metarquivo de mídia, suporte a vários idiomas
- playlists de metarquivo, suporte a vários idiomas
- playlists, suporte a vários idiomas
- Windows Playlists de metarquivo de mídia, suporte a idiomas
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002066"
---
# <a name="support-for-multiple-languages"></a>Suporte para vários idiomas

o Windows Media Player 9 Series ou posterior dá suporte a Windows metaarquivos de mídia criados usando o conjunto de caracteres Unicode. Isso permite que você inclua metadados multilíngües na sua lista de reprodução de metarquivo. as regras a seguir regem o uso de metadados multilíngues em metaarquivos de mídia Windows:

-   Os caracteres devem ser codificados usando o esquema de codificação UTF-8.
-   A lista de reprodução de metarquivo deve incluir o seguinte **parâmetro** no nível de playlist:
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   somente o Windows Media Player 9 Series ou posterior dá suporte a essa funcionalidade.
-   Se a lista de reprodução do metarquivo não for salva com codificação UTF-8 e o elemento **param** correto, ela será analisada usando a página de código padrão de localidade do sistema do computador do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Windows Visão geral dos metaarquivos de mídia**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




