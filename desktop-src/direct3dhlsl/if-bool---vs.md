---
title: se bool - vs
description: Inicia um se... Mais... endif – vs bloco.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b113c806342d786d258713128bc2cadcbb000235c2639f49e5b57ce3fa3bd2e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986526"
---
# <a name="if-bool---vs"></a>se bool - vs

Inicia um se... [else](else---vs.md)... [endif – vs](endif---vs.md) bloco.

## <a name="syntax"></a>Syntax



| se bool |
|---------|



 

em que bool é um número de registro bool. Consulte [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| se bool                |      | x    | x    | x     | x    | x     |



 

Se o registro booliana de origem na instrução if for true, o código incluído pela instrução if e a correspondência será executado. Caso contrário, o código incluído pelo [outro](else---vs.md)... [endif – as instruções vs](endif---vs.md) são executados. Essa instrução consome um slot de instrução.

se os blocos puderem ser aninhados.

Um bloco if não pode bloquear um bloco de loop.

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

[else - vs](else---vs.md)
</dt> <dt>

[endif - vs](endif---vs.md)
</dt> </dl>

 

 




