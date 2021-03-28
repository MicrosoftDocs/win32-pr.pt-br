---
title: rótulo-PS
description: Marque a próxima instrução como tendo um índice de rótulo. | rótulo-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989207"
---
# <a name="label---ps"></a>rótulo-PS

Marque a próxima instrução como tendo um índice de rótulo.

## <a name="syntax"></a>Syntax



| rótulo l\# |
|-----------|



 

onde \# o identifica o número do rótulo.

Para \_ o PS 2 \_ x, o número do rótulo deve estar entre 0 e 15.

Para \_ \_ o software PS 2 SW, PS \_ 3 \_ 0 e PS \_ 3 \_ SW, o número do rótulo deve estar entre 0 e 2047.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Esta instrução define um rótulo localizado na próxima instrução do sombreador. A instrução Label só pode ser apresentada diretamente após uma instrução [RET](ret---ps.md) (que define o fim da sub-rotina ou do programa principal anterior).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




