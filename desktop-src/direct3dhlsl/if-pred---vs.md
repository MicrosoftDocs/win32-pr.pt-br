---
title: se pred - vs
description: Início de um se pred - vs... else - vs... endif - vs block, com a condição retirada do conteúdo do registro de predicado.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad9aba5c9f18b88577a456764a71cc27637d24856cdafa95d811344034d514f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511902"
---
# <a name="if-pred---vs"></a>se pred - vs

Início de um se pred - vs... [else - vs](else---vs.md)... [endif - vs](endif---vs.md) block, com a condição retirada do conteúdo do registro de predicado.

## <a name="syntax"></a>Syntax



| se \[ ! \] pred.replicateSwizzle |
|-------------------------------|



 

Em que:

-   \[!\] um modificador NOT opcional. Isso modifica o valor no registro de predicado.
-   pred é o registro de predicado, p0. Consulte [Registro de predicado.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   replicateSwizzle é um único componente copiado (ou replicado) para todos os quatro componentes (swizzled). Os componentes válidos são: x, y, z, w ou r, g, b, a.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| se pred                |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em um canal do registro de predicado. Cada bloco \_ se pred deve terminar com uma instrução else ou endif.

As restrições incluem:

se \_ blocos pred puderem ser aninhados. Isso conta para a profundidade total de aninhamento dinâmico, juntamente com [ \_ blocos se comp.](if-comp---vs.md)

Um bloco \_ se pred não puder bloquear um bloco de loop, ele deverá estar completamente dentro dele ou cercar-o.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




