---
title: Registro de contador de loop (referência de HLSL VS)
description: Leia sobre o registro do contador de loop para sombreadores de vértice. O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405769"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Registro de contador de loop (referência de HLSL VS)

O único registro nesse banco é o registro do contador de loops atual (aL). Ele é incrementado automaticamente em cada execução do [loop-vs](loop---vs.md)... bloco [ENDLOOP-vs](endloop---vs.md) . Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




