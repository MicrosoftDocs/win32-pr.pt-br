---
title: FRC-PS
description: Retorna a parte fracionária de cada componente de entrada. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298332"
---
# <a name="frc---ps"></a>FRC-PS

Retorna a parte fracionária de cada componente de entrada.

## <a name="syntax"></a>Syntax



| FRC DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| frc                   |      |      |      |      | x    | x    | x     | x    | x     |



 

O trecho de código a seguir mostra conceitualmente como a instrução Opera.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



A função Floor converte o argumento passado para o maior inteiro que é menor que (ou igual a) do argumento. Isso é convertido em um float e, em seguida, subtraído do o valor original. O valor fracionário resultante varia de 0,0 a 1,0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




