---
description: Alocador de memória
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Alocador de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500588"
---
# <a name="memory-allocator"></a>Alocador de memória

O objeto alocador de memória aloca buffers para exemplos de mídia. Os filtros podem usar esse objeto para alocar buffers de memória compartilhada; no entanto, um filtro com requisitos especiais também pode implementar seu próprio objeto de alocador de memória. Crie esse objeto chamando **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Identificador de classe | \_MEMORYALLOCATOR CLSID                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do DirectShow](directshow-objects.md)
</dt> </dl>

 

 



