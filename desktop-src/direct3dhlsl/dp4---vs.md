---
title: dp4 – vs
description: Calcula o produto de ponto de quatro componentes dos registros de origem. | dp4 – vs
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d74c053806db14e48f41c5d3b79a67acce640a151cf696a2795a4175ccb5fc89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673846"
---
# <a name="dp4---vs"></a>dp4 – vs

Calcula o produto de ponto de quatro componentes dos registros de origem.

## <a name="syntax"></a>Syntax



| dp4 dst, src0, src1 |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dp4                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas:


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




