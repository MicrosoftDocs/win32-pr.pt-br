---
title: DST-vs
description: Calcula um vetor de distância. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837743"
---
# <a name="dst---vs"></a>DST-vs

Calcula um vetor de distância.

## <a name="syntax"></a>Syntax



| destino do DST, src0, src1 |
|----------------------|



 

onde

-   dest é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DST                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



O primeiro operando de origem (src0) é considerado como o vetor (ignorado, d d \* , d \* d, ignorado) e o segundo operando de origem (src1) é considerado como o vetor (ignorado, 1/d, ignorado, 1/d). O destino (dest) é o vetor de resultado (1, d, d \* d, 1/d).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




