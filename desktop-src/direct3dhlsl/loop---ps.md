---
title: loop - ps
description: Inicia um loop... endloop – bloco ps.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a08d2954b478bd6afd0c52d517e07a82ba3ee148dd07f839ec7d8787d93c2134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510979"
---
# <a name="loop---ps"></a>loop - ps

Inicia um loop... [endloop – bloco ps.](endloop---ps.md)

## <a name="syntax"></a>Syntax



| loop aL, i\# |
|--------------|



 

Em que:

-   aL é o Registro [de Contador de Loop que](dx9-graphics-reference-asm-ps-registers-loop-counter.md) mantém a contagem de loops atual.
-   i \# é um Registro inteiro [constante.](dx9-graphics-reference-asm-ps-registers-constant-integer.md) Consulte Observações.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   O [AL](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Registro de Contadores de Loop) contém a contagem de loops atual e pode ser usado para endereçamento relativo no Registro de Cores de Entrada [(v](dx9-graphics-reference-asm-ps-registers-input-color.md) ) dentro do bloco \# de loop.
-   i \# .x especifica a contagem de iteração. O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem diminui o valor de i \# .x.
-   i .y especifica o valor inicial do registro do Contador de \# [Loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL). O intervalo legal é \[ 0, 255 \] . Observe que essa instrução não incrementa nem diminui o valor de i \# .y.
-   i \# .z especifica o tamanho da etapa/do passo. O intervalo legal é \[ -128, 127 \] .
-   i \# .w não é usado pelo bloco de loop e deve ser 0.
-   Blocos de loop podem ser aninhados. Consulte [Flow limitações de controle.](dx9-graphics-reference-asm-ps-instructions-flow-control.md)
-   Quando aninhado, o valor do AL (Registro de Contador de [Loop)](dx9-graphics-reference-asm-ps-registers-loop-counter.md) refere-se ao bloco de loop delimitadores imediato.
-   Blocos de loop têm permissão para estar completamente dentro de um bloco if \* ou completamente ao redor dele. Não é permitido nenhum retardo.

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

 

 




