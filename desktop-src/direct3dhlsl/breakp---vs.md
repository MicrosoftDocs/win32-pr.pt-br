---
title: breakp-vs
description: Interromper condicionalmente o loop atual no ENDLOOP-vs ou endrep-vs mais próximo. Use um dos componentes do registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006890"
---
# <a name="breakp---vs"></a>breakp-vs

Interromper condicionalmente o loop atual no [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md)mais próximo. Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] P0. w.x.y.|Iar|z|Mostrar |
|-----------------------------|



 

Em que:

-   \[!\] booliano opcional não.
-   P0 é o registro de predicado. Consulte [registro de predicado](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} é o swizzle de replicação necessário em P0.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




