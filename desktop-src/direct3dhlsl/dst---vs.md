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
ms.openlocfilehash: d75eb61dd498d7a2f1d6bd9c5bd0dd9c52f3fd56625cb41b0026e9acce431ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068346"
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
| dst                    | x    | x    | x    | x     | x    | x     |



 

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

 

 




