---
title: pow-vs
description: Src0 (ABS de precisão completa) src1. | pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172662"
---
# <a name="pow---vs"></a>pow-vs

Src0 (ABS de precisão completa)<sup>src1</sup>.

## <a name="syntax"></a>Syntax



| pow DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de fonte de entrada. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.
-   src1 é um registro de fonte de entrada. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Essa instrução funciona como mostrado aqui.


```
dest = pow(abs(src0), src1);
```



Essa é uma instrução escalar, portanto, os registros de origem devem ter replicar swizzles para indicar quais canais são usados.

O resultado escalar é replicado para todos os quatro canais de saída.

Essa instrução pode ser expandida como exp ( \* log src1 (src0)).

A precisão não é inferior a 15 bits.

O registro do dest deve ser um registro temporário e não deve ser o mesmo registrado como src1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




