---
title: Registro de contador de loop (referência de HLSL VS)
description: O único registro nesse banco é o registro do contador de loops atual (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365314"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Registro de contador de loop (referência de HLSL VS)

O único registro nesse banco é o registro do contador de loops atual (aL). Ele é incrementado automaticamente em cada execução do [loop-vs](loop---vs.md)... bloco [ENDLOOP-vs](endloop---vs.md) . Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




