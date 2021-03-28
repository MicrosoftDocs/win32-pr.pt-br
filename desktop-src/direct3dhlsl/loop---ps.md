---
title: loop-PS
description: Inicia um loop... bloco ENDLOOP-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006896"
---
# <a name="loop---ps"></a>loop-PS

Inicia um loop... bloco [ENDLOOP-PS](endloop---ps.md) .

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Em que:

-   aL é o [registro de contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) que mantém a contagem de loops atual.
-   i \# é um [registro inteiro constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md). Consulte Observações.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   O [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) mantém a contagem de loops atual e pode ser usado para endereçamento relativo no [registro de cor de entrada](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) dentro do bloco de loop.
-   i \# . x especifica a contagem de iteração. O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem Decrementa o valor de i \# . x.
-   i \# . y especifica o valor inicial do registro do [contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al). O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem Decrementa o valor de i \# . y.
-   i \# . z especifica o tamanho Step/Stride. O intervalo legal é \[ -128, 127 \] .
-   i \# . w não é usado pelo bloco de loop e deve ser 0.
-   Blocos de loop podem ser aninhados. Consulte [limitações de controle de fluxo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Quando aninhado, o valor do [registro do contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (al) refere-se ao bloco de loops de circunscrição imediato.
-   Os blocos de loops podem estar completamente dentro de um \* bloco If ou completamente em torno dele. Não é permitido ampliar.

## <a name="example"></a>Exemplo


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




