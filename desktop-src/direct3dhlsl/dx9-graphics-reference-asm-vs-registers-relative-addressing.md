---
title: Endereçamento relativo (referência vs HLSL)
description: Para sombreadores de vértice, a sintaxe \ pode ser usada somente em tipos de registro que podem ser relativamente abordados em determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 82fe97a6b78a2257208f3072d5932523d5cd04ba1d044b8a57fad5f3c212b94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744336"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Endereçamento relativo (referência vs HLSL)

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



| Tipo de registro | Versões do sombreador de vértice |
|---------------|------------------------|
| a0            | Tudo                    |
| Al            | vs \_ 2 \_ 0 e superior    |
| cn            | vs \_ 1 \_ 1 e superior    |
| on            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




