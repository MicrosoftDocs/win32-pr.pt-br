---
description: SGROUPING de localidade \_
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922988"
---
# <a name="locale_sgrouping"></a>SGROUPING de localidade \_

Tamanhos de cada grupo de dígitos à esquerda do decimal. O número máximo de caracteres permitido para essa cadeia de caracteres é dez, incluindo um caractere nulo de terminação. Um tamanho explícito é necessário para cada grupo, e os tamanhos são separados por ponto e vírgula. Se o último valor for 0, o valor anterior será repetido. Por exemplo, para agrupar milhares, especifique 3; 0. As localidades em Índico agrupam os primeiros mil e depois agrupam por centenas. Por exemplo, 12, 34, 56789 é representado por 3; 2; 0.

Exemplos adicionais:



| Especificação | Cadeia de caracteres resultante   |
|---------------|--------------------|
| 3; 0           | 3.000.000.000.000  |
| 3; 2; 0         | 30, 00, 00, 00, 00000 |
| 3             | 3.000.000.000.000     |
| 3; 2           | 30000000, 00000    |



 

 

 



