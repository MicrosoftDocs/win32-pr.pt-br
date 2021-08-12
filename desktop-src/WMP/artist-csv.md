---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player online, artist.csv
- lojas online, artist.csv
- tipo 1 lojas online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4192d0817740ac872d1c08989f2f57b4715d65fea6b9a6c9a199dcdabe267e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583037"
---
# <a name="artistcsv"></a>artist.csv

Esse arquivo contém uma entrada para cada artista no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela abaixo. Os campos devem aparecer na ordem listada.

Todos os campos artist.csv são necessários.

A coluna Formato na tabela a seguir descreve como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Formato, isso significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo                  | Formatar                                            | Descrição                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | Inteiro não negativo. Exemplo: 65832              | Identificador exclusivo para o artista, exclusivo em artist.csv. Deve ser menor que 2^32.                        |
| ArtistName             | Cadeia de caracteres Unicode. Exemplo: Don Ltda<br/>       | Nome de exibição para o artista.                                                                               |
| LinkedGenreID          | Inteiro não negativo. Exemplo: 313<br/>      | GenreID do gênero principal do artista. Deve ser um gênero principal e não um subgêneo. Somente um valor é permitido. |
| LinkedSimilarArtistIDs | N/D                                               | Não usado nesta versão. Deve estar vazio.                                                                 |
| Popularidade             | Pode ser inteiro ou valor decimal. Exemplo: 1252,25 | Classificação de popularidade. Pode ser a posição na lista quando classificação por popularidade.                             |
| FeedsAvailable         | Booliano. Formato: \[ 0 \| 1 \] Exemplo: 0<br/>    | Não usado nesta versão. Deve estar vazio.                                                                 |



 

 

 





