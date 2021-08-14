---
title: RSQ-vs
description: Computa a raiz quadrada recíproca (somente positivo) do escalar de origem. | RSQ-vs
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 937f89a018943d9ab8f74a4a328316d5d68dca7d48730a06b80814dacbd8ed68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510903"
---
# <a name="rsq---vs"></a>RSQ-vs

Computa a raiz quadrada recíproca (somente positivo) do escalar de origem.

## <a name="syntax"></a>Syntax



| RSQ DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| rsq                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



O valor absoluto é obtido antes do processamento.

A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 4,0) porque implementações comuns separam mantissa e expoente.

Se a origem não tiver nenhum subscrito, o componente x será usado. A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0. Uma fonte de 0,0 gera infinitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




