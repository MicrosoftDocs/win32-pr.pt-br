---
title: sgn-vs
description: Computa o sinal da entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365236"
---
# <a name="sgn---vs"></a>sgn-vs

Computa o sinal da entrada.

## <a name="syntax"></a>Syntax



| sgn DST, src0, src1, src2 |
|---------------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro temporário que contém resultados intermediários. Após a execução, os conteúdos são indefinidos.
-   src2 é um registro temporário que contém resultados intermediários. Após a execução, os conteúdos são indefinidos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Sgn                    |      | x    | x    | x     | x    | x     |



 

Essa instrução funciona conforme mostrado abaixo.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 e src2 devem ser diferentes s de [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




