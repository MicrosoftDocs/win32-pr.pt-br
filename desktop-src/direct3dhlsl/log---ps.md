---
title: log-PS
description: ₂ de log de precisão total (x). | log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968520"
---
# <a name="log---ps"></a>log-PS

₂ de log de precisão total (x).

## <a name="syntax"></a>Syntax



| hora de log, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem. O registro de origem requer uso explícito de replicate swizzle; ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou o. r,. g,. b,. equivalentes) deve ser especificado.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| log                   |      |      |      |      | x    | x    | x     | x    | x     |



 

O trecho de código a seguir mostra as operações executadas.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Essa instrução aceita uma fonte escalar cujo bit de sinal é ignorado. O resultado é replicado para todos os quatro canais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




