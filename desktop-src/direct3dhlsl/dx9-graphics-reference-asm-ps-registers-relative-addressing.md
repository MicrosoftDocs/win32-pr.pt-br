---
title: Endereçamento relativo (referência do HLSL PS)
description: A sintaxe \ \ pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638911"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Endereçamento relativo (referência do HLSL PS)

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



| Tipo de registro                                                                                   | Versões do sombreador de pixel |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al nos registros de entrada | PS \_ 3 \_ 0 e superior   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




