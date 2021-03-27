---
title: FRC-vs
description: Retorna a parte fracionária de cada componente de entrada. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298331"
---
# <a name="frc---vs"></a>FRC-vs

Retorna a parte fracionária de cada componente de entrada.

## <a name="syntax"></a>Syntax



| FRC DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| frc                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra conceitualmente como a instrução Opera.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



A função Floor converte o argumento passado para o maior inteiro que é menor que (ou igual a) do argumento. Isso é convertido em um float e, em seguida, subtraído do o valor original. O valor fracionário resultante varia de 0,0 a 1,0.

Para a versão 1 \_ 1, as máscaras de gravação permitidas são. s e. XY (. x não é permitido).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




