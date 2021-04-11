---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Armazenamentos online do Windows Media Player, artist.csv
- lojas online, artist.csv
- Digite 1 lojas online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292796"
---
# <a name="artistcsv"></a>artist.csv

Esse arquivo contém uma entrada para cada artista no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

Todos os campos em artist.csv são obrigatórios.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo                  | Formatar                                            | Descrição                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Artistaid               | Inteiro não negativo. Exemplo: 65832              | Identificador exclusivo para o artista, exclusivo dentro do artist.csv. Deve ser menor que 2 ^ 32.                        |
| ArtistName             | Cadeia de caracteres Unicode. Exemplo: Don funk<br/>       | Nome de exibição do artista.                                                                               |
| LinkedGenreID          | Inteiro não negativo. Exemplo: 313<br/>      | Gêneroid do gênero principal do artista. Deve ser um gênero principal e não um subgênero. Apenas um valor é permitido. |
| LinkedSimilarArtistIDs | N/D                                               | Não usado nesta versão. Deve estar vazio.                                                                 |
| Popularidade             | Pode ser um valor inteiro ou Decimal. Exemplo: 1252,25 | Classificação de popularidade. Pode ser a posição na lista quando classificada por popularidade.                             |
| FeedsAvailable         | Booliano. Formato: \[ 0 \| 1 \] exemplo: 0<br/>    | Não usado nesta versão. Deve estar vazio.                                                                 |



 

 

 





