---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Armazenamentos online do Windows Media Player, genre.csv
- lojas online, genre.csv
- Digite 1 lojas online, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916482"
---
# <a name="genrecsv"></a>genre.csv

Esse arquivo contém uma entrada para cada gênero representado no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

Todos os campos em genre.csv são obrigatórios.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo             | Formatar                                                    | Descrição                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do gênero \_         | Inteiro não negativo. Exemplo: 22<br/>               | Identificador de gênero, exclusivo dentro de genre.csv. Deve ser menor que 2 ^ 32. Um máximo de 64 gêneros é possível.                                             |
| GenreTitle        | Cadeia de caracteres Unicode. Exemplo: Rock<br/>                   | Nome de exibição do gênero.                                                                                                                                |
| FeedsAreAvailable | Booliano. formato: \[ 0 \| 1\]<br/> Exemplo: 0<br/> | Indica se o comportamento de "toque de rádio" é possível ao saltar para um feed.                                                                          |
| HasComposer       | Booliano. formato: \[ 0 \| 1\]<br/> Example: 1<br/> | True se este gênero deve salvar informações do compositor no catálogo. Se não estiver definido, as informações do Composer serão ignoradas e não compiladas no catálogo. |



 

 

 





