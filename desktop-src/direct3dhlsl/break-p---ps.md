---
title: breakp-PS
description: Interromper condicionalmente o loop atual no ENDLOOP-PS ou endrep-PS mais próximo. Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365244"
---
# <a name="breakp---ps"></a>breakp-PS

Interromper condicionalmente o loop atual no [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)mais próximo. Use um dos componentes de registro de predicado como uma condição para determinar se deseja ou não realizar a instrução.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] P0. w.x.y.|Iar|z|Mostrar |
|-----------------------------|



 

Em que:

-   \[!\] é um modificador opcional de negação.
-   P0 é o [registro de predicado](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} é o swizzle de replicação necessário em P0.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




