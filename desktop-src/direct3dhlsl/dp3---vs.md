---
title: DP3-vs
description: Computa o produto de três componentes do ponto dos registros de origem. | DP3-vs
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf65f77a60ea7ac19ef5ea204f916387c65c3bee08c89ea274e800f650ef241d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673866"
---
# <a name="dp3---vs"></a>DP3-vs

Computa o produto de três componentes do ponto dos registros de origem.

## <a name="syntax"></a>Syntax



| DP3 DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| dp3                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas:


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




