---
title: mul - ps
description: Multiplica fontes no destino. | mul - ps
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 74ff42065f7b41c1d775a0b1924d732110c31bd3121d2464b33eb8b20ae31e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986296"
---
# <a name="mul---ps"></a>mul - ps

Multiplica fontes no destino.

## <a name="syntax"></a>Syntax



| mul dst, src0, src1 |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| mul                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

O snippet de código a seguir mostra as operações executadas.


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




