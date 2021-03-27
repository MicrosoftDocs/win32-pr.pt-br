---
title: loop-vs
description: Iniciar um loop... bloco ENDLOOP.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988590"
---
# <a name="loop---vs"></a>loop-vs

Iniciar um loop... bloco [ENDLOOP](endloop---vs.md) .

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Em que:

-   aL é o [registro de contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) que mantém a contagem de loops atual.
-   i \# é um [registro inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md). Consulte Observações.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   O [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) mantém a contagem de loops atual e pode ser usado para endereçamento relativo em c ( [registro inteiro constante](dx9-graphics-reference-asm-vs-registers-constant-integer.md) \# ) ou [registros de saída](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) dentro do bloco de loop.
-   i \# . x especifica a contagem de iteração. O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.
-   i \# . y especifica o valor inicial do registro do [contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al). O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem Decrementa o valor de i \# . y.
-   i \# . z especifica o tamanho Step/Stride. O intervalo legal é \[ -128, 127 \] .
-   i \# . w não é usado e deve ser definido como 0.
-   Blocos de loop podem ser aninhados. Consulte [limites de aninhamento de controle de fluxo](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Quando aninhado, o valor do [registro do contador de loop](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (al) refere-se ao bloco de loops de circunscrição imediato.
-   Os blocos de loops podem estar completamente dentro de um \* bloco If ou completamente em torno dele. Não é permitido ampliar.

## <a name="example"></a>Exemplo


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




