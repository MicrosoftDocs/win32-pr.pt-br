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
ms.openlocfilehash: fcabc6dcf5043c23be252fe6ac25c99da505e33b7c670c95ee5672b50ddb74bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744626"
---
# <a name="input-color-register"></a>Registro de cor de entrada

Registro de entrada do sombreador de pixel que contém a cor do vértice.

## <a name="syntax"></a>Syntax


```
dcl v#.writeMask
```



em que:

-   [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) é uma instrução de declaração de registro.
-   v é um registro de entrada \# e é o número do registro. O número de registros permitidos é determinado pela versão do sombreador.
-   writeMask determina quais componentes (até quatro) são gravados. Os componentes válidos são: (x,y, z,w) ou (r,g,b,a).

## <a name="remarks"></a>Comentários

Registros de cores são registros somente leitura. Cada registro contém valores RGBA de quatro componentes iterados de vértices de entrada. Eles têm uma precisão menor do que a maioria dos registros, com garantia de ter 8 bits de dados não assinados no intervalo (0, +1). Você não pode usar mais de um em uma única instrução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 \_ \_ ps \_ 1 \_ 3 \_ \_ ps \_ 1 \_ 4 Registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[ps \_ 2 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[ps \_ 2 \_ x Registers](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[ps \_ 3 \_ 0 Registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




