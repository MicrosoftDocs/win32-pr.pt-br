---
title: se bool-PS
description: Início de um bloco If.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638853"
---
# <a name="if-bool---ps"></a>se bool-PS

Início de um bloco If.

## <a name="syntax"></a>Syntax



| se bool |
|---------|



 

Em que:

-   bool é um número de registro bool (booliano). Consulte [constante de registro booliano](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| se bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Se o registro booliano de origem na instrução If for true, o código incluído na instrução If e o [endif-PS](endif---ps.md) ou [else-PS](else---ps.md) correspondente serão executados. Caso contrário, o código incluído pelo else-PS... endif-instruções PS são executadas. Essa instrução consome um slot de instrução.

Um bloco If pode ser aninhado.

Um bloco If não pode ampliar um bloco de loop.

Um bloco If pode ser seguido por um bloco de instruções e/ou uma instrução [else-PS](else---ps.md) e/ou uma instrução [endif-PS](endif---ps.md) .

## <a name="example"></a>Exemplo

Essa instrução fornece controle de fluxo estático condicional.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else-PS](else---ps.md)
</dt> <dt>

[endif-PS](endif---ps.md)
</dt> </dl>

 

 




