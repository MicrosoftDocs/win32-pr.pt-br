---
title: pow-PS
description: Src0 (ABS de precisão completa) src1. | pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968330"
---
# <a name="pow---ps"></a>pow-PS

Src0 (ABS de precisão completa)<sup>src1</sup>.

## <a name="syntax"></a>Syntax



| pow DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de fonte de entrada. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.
-   src1 é um registro de fonte de entrada. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Essa instrução funciona da seguinte maneira:

dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;

Essa é uma instrução escalar, portanto, os registros de origem devem ter replicar swizzles para indicar quais canais são usados.

A potência de entrada (src1) deve ser um escalar.

O resultado escalar é replicado para todos os quatro canais de saída.

Essa instrução pode ser expandida como exp ( \* log src1 (src0)).

O registro de hora de verão deve ser um registro temporário e não deve ser o mesmo registrado como src1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




