---
title: Modificadores de instrução (referência de HLSL VS)
description: Modificadores de instrução
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2bdad90d13fe960c0d7a5cabfbb508d8abba890e8114c6d4ae1e47d1977e7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119690"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a>Modificadores de instrução (referência de HLSL VS)

Os modificadores de instrução afetam o resultado da instrução antes de serem gravados no registro de destino.

## <a name="_sat"></a>\_saturação

Satura (ou coloca) o resultado da instrução para \[ 0, 1 \] intervalo antes de gravar no registro de destino.

Por exemplo:


```
add_sat dst, src0, src1
```



Em que:

DST = fixe \_ entre \_ 0 \_ e \_ 1 (src0 + src1)

O \_ modificador de instrução SAT não custa nenhum slot de instrução adicional.

Se houver suporte, o \_ modificador de instrução SAT pode ser usado com qualquer instrução, exceto: [FRC-vs](frc---vs.md), [Sincos-vs](sincos---vs.md)e [texldl-vs](texldl---vs.md).



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_saturação                  |      |      |      |       | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




