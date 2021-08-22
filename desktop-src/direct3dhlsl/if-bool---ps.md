---
title: se bool - ps
description: Início de um bloco if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457506"
---
# <a name="if-bool---ps"></a>se bool - ps

Início de um bloco if.

## <a name="syntax"></a>Sintaxe



| se bool |
|---------|



 

Em que:

-   bool é um número de registro bool (booliana). Consulte [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| se bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Se o registro booliana de origem na instrução if for true, o código incluído pela instrução if e o endif correspondente [– ps](endif---ps.md) ou , [ps](else---ps.md) será executado. Caso contrário, o código incluído pelo outro – ps... endif – as instruções ps são executadas. Essa instrução consome um slot de instrução.

Um bloco if pode ser aninhado.

Um bloco if não pode bloquear um bloco de loop.

Um bloco if pode ser seguido por um bloco de instrução e/ou outro [- instrução ps](else---ps.md) e/ou [uma instrução endif - ps.](endif---ps.md)

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

[else - ps](else---ps.md)
</dt> <dt>

[endif - ps](endif---ps.md)
</dt> </dl>

 

 




