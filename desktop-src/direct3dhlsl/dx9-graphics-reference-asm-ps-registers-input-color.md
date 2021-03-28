---
title: Registro de cor de entrada
description: Registro de entrada do sombreador de pixel que contém a cor do vértice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364484"
---
# <a name="input-color-register"></a>Registro de cor de entrada

Registro de entrada do sombreador de pixel que contém a cor do vértice.

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



em que:

-   [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) é uma instrução de declaração de registro.
-   v é um registro de entrada e \# é o número de registro. O número de registros permitidos é determinado pela versão do sombreador.
-   writeMask determina quais componentes (até quatro) são gravados. Os componentes válidos são: (x, y, z, w) ou (r, g, b, a).

## <a name="remarks"></a>Comentários

Os registros de cores são registros somente leitura. Cada registrador contém valores RGBA de quatro componentes iterados a partir de vértices de entrada. Eles têm uma precisão menor do que a maioria dos registros, garantindo que tenham 8 bits de dados não assinados no intervalo (0, + 1). Você não pode usar mais de um em uma única instrução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registros PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registros PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registros PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




