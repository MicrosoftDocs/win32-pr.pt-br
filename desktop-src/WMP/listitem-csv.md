---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Armazenamentos online do Windows Media Player, listitem.csv
- lojas online, listitem.csv
- Digite 1 lojas online, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363865"
---
# <a name="listitemcsv"></a>listitem.csv

Esse arquivo contém entradas para cada item incluído em uma lista. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

Todos os campos são obrigatórios.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo              | Formatar                                          | Descrição                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| \_ListId vinculado     | Inteiro não negativo. Exemplo: 465<br/>    | A ID da lista da qual este item faz parte.                                                                               |
| \_ListItem vinculado   | Inteiro não negativo. Exemplo: 684793<br/> | O ID do item. Pode ser a ID de uma faixa, um álbum, um artista, um gênero, um subgênero, um feed de rádio ou outra lista. |
| ItemPositionInList | Inteiro não negativo. Exemplo: 5<br/>      | A posição do item dentro de sua lista. O primeiro item em uma lista está na posição 0.                                   |



 

 

 





