---
description: Alocador de memória
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Alocador de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909414"
---
# <a name="memory-allocator"></a>Alocador de memória

O objeto alocador de memória aloca buffers para exemplos de mídia. Os filtros podem usar esse objeto para alocar buffers de memória compartilhada; no entanto, um filtro com requisitos especiais também pode implementar seu próprio objeto de alocador de memória. Crie esse objeto chamando **CoCreateInstance**.



| Label | Valor |
|------------------|----------------------------------------|
| Identificador de classe | \_MEMORYALLOCATOR CLSID                 |
| Interfaces       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do DirectShow](directshow-objects.md)
</dt> </dl>

 

 



