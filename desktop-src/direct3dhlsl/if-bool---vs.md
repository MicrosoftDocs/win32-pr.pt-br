---
title: se bool-vs
description: Inicia um if... senão... endif – bloco vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006862"
---
# <a name="if-bool---vs"></a>se bool-vs

Inicia um if... [senão](else---vs.md)... [endif – bloco vs](endif---vs.md) .

## <a name="syntax"></a>Syntax



| se bool |
|---------|



 

em que bool é um número de registro bool. Consulte [constante de registro booliano](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| se bool                |      | x    | x    | x     | x    | x     |



 

Se o registro booliano de origem na instrução If for true, o código incluído na instrução If e a outra correspondência serão executados. Caso contrário, o código incluído no [else](else---vs.md)... [endif-](endif---vs.md) as instruções vs são executadas. Essa instrução consome um slot de instrução.

se blocos podem ser aninhados.

Um bloco If não pode ampliar um bloco de loop.

## <a name="example"></a>Exemplo

Essa instrução fornece controle de fluxo estático condicional.


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[else-vs](else---vs.md)
</dt> <dt>

[endif-vs](endif---vs.md)
</dt> </dl>

 

 




