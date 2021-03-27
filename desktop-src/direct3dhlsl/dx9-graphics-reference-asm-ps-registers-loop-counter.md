---
title: Registro de contador de loop (referência do HLSL PS)
description: O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638915"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro de contador de loop (referência do HLSL PS)

O único registro nesse banco é o registro do contador de loops atual (aL). Ele é incrementado automaticamente em cada execução do bloco de [bits do loop PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de contador de loop |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




