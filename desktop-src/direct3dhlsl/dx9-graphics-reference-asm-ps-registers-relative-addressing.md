---
title: Endereçamento relativo (referência de PS HLSL)
description: Para sombreadores de pixel, a sintaxe \ pode ser usada somente em tipos de registro que podem ser relativamente abordados em determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405479"
---
# <a name="relative-addressing-hlsl-ps-reference"></a>Endereçamento relativo (referência de PS HLSL)

A sintaxe pode ser usada somente em tipos de registro que podem ser relativamente abordados \[ \] em determinados modelos de sombreador. As formas de sintaxe com \[ \] suporte são listadas da seguinte forma:

Em que:

-   "R" indica qualquer tipo de registro que possa ser relativamente resolvido.
-   "A" indica qualquer registro que possa ser usado como um índice para resolver relativamente outros registros.
-   n0 - ni, m0 - mj e k são inteiros >= 0.



| \[\]sintaxe                              | Índice efetivo                       | Exemplos                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + m0 + ... + mj \]                  | A + m0 + ... + mj                     | c \[ a0.x + 3 + 7 \]              |
| R \[ k ( = \] Rk )                         | k                                     | c \[ 10 \] ( = c10 )              |
| R \[ A \]                                  | Um                                     | c \[ a0.y \]                      |
| Rk \[ n0 + ... + ni + A + m0 + ... + mj \] | A + k + n0 + ... + ni + m0 + ... + mj | c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \] |
| R \[ n0 + ... + ni + A + m0 + ... + mj \]  | A + n0 + ... + ni + m0 + ... + mj     | c \[ 2 + 1 + aL + 3 + 4 + 5 \]    |
| Rk \[ A \]                                 | A + k                                 | c12 \[ aL \] , c0 \[ a0.z \]        |
| Rk \[ A + m0 + ... + mj \]                 | A + k + m0 + ... + mj                 | v1 \[ aL + 4 + 8 \]               |
| R \[ n0 + ... + ni + A \]                  | A + n0 + ... + ni                     | o \[ 3 + 1 + aL \]                |
| Rk \[ n0 + ... + ni + A \]                 | A + k + n0 + ... + ni                 | o1 \[ 2 + 1 + 3 + aL \]           |



 

Os registros estão disponíveis nas seguintes versões:



| Tipo de registro                                                                                   | Versões do Sombreador de Pixel |
|-------------------------------------------------------------------------------------------------|-----------------------|
| [contador de loop:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL em registros de entrada | ps \_ 3 \_ 0 e superior   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




