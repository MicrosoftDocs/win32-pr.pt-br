---
title: Registro de contador de loop (referência de PS HLSL)
description: Leia sobre o registro do contador de loop para sombreadores de pixel. O único registro nesse banco é o registro do contador de loop atual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405509"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro de contador de loop (referência de PS HLSL)

O único registro nesse banco é o registro do contador de loop atual (aL). Ele é incrementado automaticamente em cada execução do [loop – ps](loop---ps.md) / [endloop – bloco ps.](endloop---ps.md) Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e é inválido para usá-lo fora do loop.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de contador de loop |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




