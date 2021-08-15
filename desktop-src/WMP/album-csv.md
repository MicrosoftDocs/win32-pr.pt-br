---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player lojas online album.csv
- lojas online, album.csv
- Digite 1 lojas online, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750926a3d01f8d65d7ed11c69436049e39ea3dabf0e446ede8a8c9dcecc53bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004196"
---
# <a name="albumcsv"></a>album.csv

Esse arquivo contém uma entrada para cada álbum incluído no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

Todos os campos em album.csv são obrigatórios.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo             | Formatar                                                                   | Descrição                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Inteiro não negativo. Exemplo: 789456<br/>                          | Identificador para o álbum, exclusivo dentro de album.csv. Deve ser menor que 2 ^ 32.                                                                                                                                                                           |
| Albumname         | Cadeia de caracteres Unicode. Exemplo: melhores ocorrências<br/>                         | Título do álbum                                                                                                                                                                                                                                          |
| AlbumArtist       | Inteiro não negativo. Exemplo: 34331<br/>                           | Artistaid do artista. Apenas um valor é permitido. Pode ser a ID de "vários artistas" ou semelhante.                                                                                                                                                    |
| AlbumLabel        | Cadeia de caracteres Unicode. Deve estar vazio.                                         | Não usado nesta versão. Deve estar vazio.                                                                                                                                                                                                           |
| Liberado       | Cadeia de caracteres Unicode, no formato AAAA-MM-DD. Exemplo: 2005-0-0<br/>        | Data de lançamento. O valor 0 é permitido para o dia ou o mês.                                                                                                                                                                                               |
| AlbumPrice        | StringExample Unicode: $12.49<br/>                                 | Preço do álbum. O símbolo de moeda deve ser incluído. A cadeia de caracteres vazia, 0 e-ter significado especial. Uma cadeia de caracteres vazia indica um preço desconhecido. ' 0 ' indica que a faixa é gratuita. Um hífen ('-') indica que o álbum não pode ser comprado. |
| LinkedGenreID     | Inteiro não negativo. Exemplo: 12<br/>                              | ID do gênero principal para o álbum. Apenas um valor é permitido.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Formato: n; n; n; Exemplo: 32; 44; 663;<br/>                             | Lista de IDs de subgêneros associadas. Um ponto e vírgula à direita é permitido no final da lista.                                                                                                                                                             |
| Popularidade        | Pode ser um valor inteiro ou decimal não negativo. Exemplo: 1256,24<br/> | Classificação de popularidade determinada pelo serviço. Pode ser a classificação deste álbum na lista de álbuns classificados por popularidade. 0 é permitido.                                                                                                              |
| IsRecentlyAdded   | Booliano. Pode ser 0 ou 1.                                                  | Sinalizador para indicar que o álbum foi adicionado recentemente, conforme determinado pelo serviço.                                                                                                                                                                    |
| Isfeatured        | Booliano. Pode ser 0 ou 1.                                                  | Sinalizador para indicar que este é um álbum em destaque.                                                                                                                                                                                                      |
| EditorialGlyph    | Inteiro não negativo. Deve ser 0.                                       | Não usado é versão. Deve ser 0.                                                                                                                                                                                                                    |
| FeedsAreAvailable | Booliano. Pode ser 0 ou 1.                                                  | Não usado nesta versão. Deve ser 0.                                                                                                                                                                                                               |



 

 

 





