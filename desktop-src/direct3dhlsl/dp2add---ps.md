---
title: dp2add – ps
description: Executa um produto de ponto 2D e uma adição escalar.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39a7cd640de57f2f69c8ee3b46ee6be6e52cbb16f9db39ef902725241d77b9c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068356"
---
# <a name="dp2add---ps"></a>dp2add – ps

Executa um produto de ponto 2D e uma adição escalar.

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Em que:

-   dst é um registro de destino.
-   src0, src1 e src2 são três registros de origem.
-   {x \| y \| z \| w} é o swizzle de replicação necessário no src2.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

O valor escalar para adicionar é escolhido pelo swizzle de replicação em src2.

O snippet de código a seguir mostra as operações executadas.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




