---
title: rsq - vs
description: Calcula a raiz recíproca quadrada (somente positiva) do escalar de origem. | rsq - vs
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
# <a name="rsq---vs"></a>rsq - vs

Calcula a raiz recíproca quadrada (somente positiva) do escalar de origem.

## <a name="syntax"></a>Syntax



| rsq dst, src |
|--------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem. O registro de origem requer o uso explícito do swizzle de replicação, ou seja, exatamente um dos componentes .x, .y, .z, .w swizzle (ou os equivalentes .r, .g, .b, .a).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
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



O valor absoluto é tirado antes do processamento.

A precisão deve ser pelo menos 1,0/(2 Vezes) erro absoluto no intervalo (1,0, 4,0) porque implementações comuns separarão mantissa e expoente.

Se a origem não tiver subscritos, o componente x será usado. A saída deverá ser exatamente 1,0 se a entrada for exatamente 1,0. Uma fonte de 0,0 produz infinito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




