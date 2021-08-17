---
title: Mad-vs
description: Multiplica e adiciona fontes.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a42a4f2d28ed8f0506909199b4c15c26ae3bc434ec250ddae9909ef53525583b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986396"
---
# <a name="mad---vs"></a>Mad-vs

Multiplica e adiciona fontes.

## <a name="syntax"></a>Syntax



| Mad DST, src0, src1, src2 |
|---------------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.
-   src2 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Mad                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




