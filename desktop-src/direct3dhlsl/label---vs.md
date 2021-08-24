---
title: rótulo – vs
description: Marque a próxima instrução como tendo um índice de rótulo. | rótulo – vs
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81c36c3db93acdc82d725c9cf7893c52d7177bbe70e16378c3b86f39ec4d6a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854176"
---
# <a name="label---vs"></a>rótulo – vs

Marque a próxima instrução como tendo um índice de rótulo.

## <a name="syntax"></a>Syntax



| rótulo l\# |
|-----------|



 

onde \# o identifica o número do rótulo.

Para vs \_ 2 \_ 0 e vs \_ 2 \_ x, o número do rótulo deve estar entre 0 e 15.

Para \_ o vs 2 \_ SW, vs \_ 3 \_ 0 e vs \_ 3 \_ SW, o número do rótulo deve estar entre 0 e 2047.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Esta instrução define um rótulo localizado na próxima instrução do sombreador. A instrução Label só pode ser apresentada diretamente após uma instrução [RET](ret---vs.md) (que define o fim da sub-rotina ou do programa principal anterior).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




