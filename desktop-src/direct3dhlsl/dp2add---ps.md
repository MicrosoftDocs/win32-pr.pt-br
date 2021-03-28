---
title: dp2add-PS
description: Executa um produto 2D dot e uma adição escalar.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084257"
---
# <a name="dp2add---ps"></a>dp2add-PS

Executa um produto 2D dot e uma adição escalar.

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Em que:

-   o DST é um registro de destino.
-   src0, src1 e src2 são três registros de origem.
-   {x \| y \| z \| w} é o swizzle de replicação necessário em src2.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

O valor escalar para Add é escolhido pelo swizzle replicate em src2.

O trecho de código a seguir mostra as operações executadas.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




