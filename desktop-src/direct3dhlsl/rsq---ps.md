---
title: RSQ-PS
description: Computa a raiz quadrada recíproca (somente positivo) do escalar de origem. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968400"
---
# <a name="rsq---ps"></a>RSQ-PS

Computa a raiz quadrada recíproca (somente positivo) do escalar de origem.

## <a name="syntax"></a>Syntax



| RSQ DST, src |
|--------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem. O registro de origem requer uso explícito de replicate swizzle, ou seja, exatamente um dos componentes. x,. y,. z,. w swizzle (ou. r,. g,. b,. equivalentes) devem ser especificados.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rsq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

O valor absoluto é obtido antes do processamento.

A precisão deve ser pelo menos 1,0/(2 ²) erro absoluto durante o intervalo (1,0, 4,0) porque implementações comuns separam mantissa e expoente.

A saída deve ser exatamente 1,0 se a entrada for exatamente 1,0. Uma fonte de 0,0 gera infinitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




