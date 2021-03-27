---
title: se Pred-PS
description: Início de um booliano-PS... else-PS... endif – bloco PS, com a condição retirada do conteúdo do registro de predicado.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638860"
---
# <a name="if-pred---ps"></a>se Pred-PS

Início de um [booliano-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif – bloco PS](endif---ps.md) , com a condição retirada do conteúdo do registro de predicado.

## <a name="syntax"></a>Syntax



| Se \[ ! \] pred. replicateSwizzle |
|-------------------------------|



 

Em que:

-   \[!\] é um modificador NOT opcional. Isso modifica o valor no registro de predicado.
-   Pred é o [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   replicateSwizzle é um componente único que é copiado (ou replicado) para todos os quatro componentes (swizzled). Os componentes válidos são: \[ x, y, z, w \] ou \[ r, g, b, a \] .

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Se \_ Pred              |      |      |      |      |      | x    | x     | x    | x     |



 

Essa instrução é usada para ignorar um bloco de código, com base em um canal do registro de predicado. Cada \_ bloco If Pred deve terminar com uma instrução [else-PS](else---ps.md) ou [endif-PS](endif---ps.md) .

As restrições incluem:

Se \_ blocos Pred puderem ser aninhados. Isso conta com a profundidade de aninhamento dinâmico total, juntamente com os blocos de [ \_ comp](if-comp---ps.md) .

Um \_ bloco If Pred não pode ampliar um bloco de loops; ele deve estar completamente dentro dele ou colocá-lo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




