---
title: RCP-vs
description: Computa o recíproco do escalar de origem. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968518"
---
# <a name="rcp---vs"></a>RCP-vs

Computa o recíproco do escalar de origem.

## <a name="syntax"></a>Syntax



| RCP DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0. Uma fonte de 0,0 gera infinitos.

A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 2,0) porque implementações comuns separam mantissa e expoente.

Se a origem não tiver nenhum subscrito, o componente x será usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




