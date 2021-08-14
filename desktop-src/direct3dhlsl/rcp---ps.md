---
title: rcp - ps
description: Calcula o recíproco do escalar de origem. | rcp - ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fba443d4a2e05794f8c1965e46a61c65edae50b95845f0f80faa0c0ab6c6bf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510951"
---
# <a name="rcp---ps"></a>rcp - ps

Calcula o recíproco do escalar de origem.

## <a name="syntax"></a>Syntax



| rcp dst, src |
|--------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem. O registro de origem requer o uso explícito do swizzle de replicação, ou seja, exatamente um dos componentes .x, .y, .z, .w swizzle (ou os equivalentes .r, .g, .b, .a).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

A saída deverá ser exatamente 1,0 se a entrada for exatamente 1,0. Uma fonte de 0,0 produz infinito.

O resultado escalar é replicado para todos os canais na máscara de gravação de destino.

A precisão deve ser pelo menos 1,0/(2 Vezes) erro absoluto no intervalo (1,0, 2,0) porque implementações comuns separarão mantissa e expoente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




