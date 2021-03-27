---
title: CRS-vs
description: Computa um produto cruzado usando a regra do lado direito. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298161"
---
# <a name="crs---vs"></a>CRS-vs

Computa um produto cruzado usando a regra do lado direito.

## <a name="syntax"></a>Syntax



| CRS DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| CRS                    |      | x    | x    | x     | x    | x     |



 

Essa instrução funciona como mostrado aqui.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Algumas restrições ao uso:

-   src0 não pode ser o mesmo registro que dest.
-   src1 não pode ser o mesmo registro que dest.
-   src0 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).
-   src1 não pode ter nenhum swizzle diferente do swizzle padrão (. xyzw).
-   o dest precisa ter exatamente uma das sete máscaras a seguir:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.
-   o dest deve ser um registro temporário.
-   dest não deve ser o mesmo registro que src0 ou src1

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




