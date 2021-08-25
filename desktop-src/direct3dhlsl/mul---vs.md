---
title: Mul-vs
description: Multiplica as fontes no destino. | Mul-vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d14603f077ddc61287d8d22580b161b59ddf8c6b67dad62141ecf4afb44d1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023756"
---
# <a name="mul---vs"></a>Mul-vs

Multiplica as fontes no destino.

## <a name="syntax"></a>Syntax



| Mul DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| mul                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




