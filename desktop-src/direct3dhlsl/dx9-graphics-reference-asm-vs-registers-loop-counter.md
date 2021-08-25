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
ms.openlocfilehash: aa0bf4d44d33f6939c8c45af4509e15e96adf9c4c36a611e049097120db2ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023936"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Registro de contador de loop (referência de HLSL VS)

O único registro nesse banco é o registro do contador de loops atual (aL). Ele é incrementado automaticamente em cada execução do [loop-vs](loop---vs.md)... bloco [ENDLOOP-vs](endloop---vs.md) . Portanto, ele pode ser usado no bloco para endereçamento relativo, se necessário, e inválido para usá-lo fora do loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




