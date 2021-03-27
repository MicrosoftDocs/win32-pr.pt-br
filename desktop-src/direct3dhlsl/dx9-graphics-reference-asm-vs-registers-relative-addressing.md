---
title: Endereçamento relativo (referência de HLSL VS)
description: A sintaxe \ \ pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293608"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Endereçamento relativo (referência de HLSL VS)

A \[ \] sintaxe pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador. As formas de sintaxe com suporte \[ \] são listadas da seguinte maneira:

Em que:

-   "R" denota qualquer tipo de registro que possa ser relativamente endereçado.
-   "A" denota qualquer registro que possa ser usado como um índice para endereçar relativamente outros registros.
-   N0-Ni, M0-MJ e k são inteiros >= 0.



| \[\]sintaxe do                              | Índice efetivo                       | Exemplos                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + M0 +... + MJ \]                  | A + M0 +... + MJ                     | c \[ a0 x + 3 + 7 \]              |
| R \[ k \] (= r)                         | k                                     | c \[ 10 \] (= C10)              |
| R \[ A \]                                  | Um                                     | c \[ a0. y \]                      |
| R \[ N0 +... + ni + A + M0 +... + MJ \] | A + k + N0 +... + ni + M0 +... + MJ | C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ N0 +... + ni + A + M0 +... + MJ \]  | A + N0 +... + ni + M0 +... + MJ     | c \[ 2 + 1 + al + 3 + 4 + 5 \]    |
| R \[ A \]                                 | A + k                                 | C12 \[ Al \] , C0 \[ a0. z \]        |
| R \[ A + M0 +... + MJ \]                 | A + k + M0 +... + MJ                 | v1 \[ al + 4 + 8 \]               |
| R \[ N0 +... + ni + A \]                  | A + N0 +... + ni                     | o \[ 3 + 1 + al \]                |
| R \[ N0 +... + ni + A \]                 | A + k + N0 +... + ni                 | O1 \[ 2 + 1 + 3 + Al \]           |



 

Os registros estão disponíveis nas seguintes versões:



| Tipo de registro | Versões do sombreador de vértice |
|---------------|------------------------|
| a0            | Tudo                    |
| &            | vs \_ 2 \_ 0 e superior    |
| cn            | vs \_ 1 \_ 1 e superior    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




