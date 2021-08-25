---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player lojas online subgenre.csv
- lojas online, subgenre.csv
- Digite 1 lojas online, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122936"
---
# <a name="subgenrecsv"></a>subgenre.csv

Esse arquivo contém uma entrada para cada subgênero representado no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo             | Obrigatório | Formatar                                                                                            | Descrição                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Subgêneroid        | Sim      | Inteiro não negativo.                                                                             | Identificador de subgênero (ID), exclusivo dentro de subgenre.csv. Até 1024 subgêneros são permitidos.                                                                   |
| SubGenreTitle     | Sim      | Cadeia de caracteres Unicode. Exemplo: música de dança inteligente (IDM)<br/>                                  | Nome de exibição do subgênero.                                                                                                                                    |
| SubGenreSubtitle  | Não       | Cadeia de caracteres Unicode. Exemplo: novo, percussive música eletrônica que não é tão puro cair.<br/> | Descreva o significado do nome de exibição do subgênero. Deve ter menos de 64 caracteres.                                                                     |
| FeedsAreAvailable | Sim      | Booliano. formato: \[ 0 \| 1\]<br/> Exemplo: 0<br/>                                         | Indica se a "reprodução de rádio" é possível ao saltar para um feed.                                                                                          |
| \_Gênero vinculado   | Sim      | Inteiro não negativo (Gêneroid). Exemplo: 12<br/>                                             | A Gêneroid do gênero pai. Somente um pai é permitido.                                                                                              |
| SortOrderRank     | Sim      | Inteiro não negativo. Exemplo: 23<br/>                                                       | Uma classificação, idealmente exclusiva, usada para classificar subgêneros na interface do usuário. Se o gênero pai tiver 10 subgêneros, isso poderá ser um inteiro de 1 a 10. |



 

 

 





