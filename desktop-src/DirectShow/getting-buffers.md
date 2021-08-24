---
description: Obter buffers
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Obter buffers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f727045142b9432da93511ecea1f3238aa24ad213fdc7715f5e2e45a91ab19a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536896"
---
# <a name="getting-buffers"></a>Obter buffers

Se o filtro tiver um alocador personalizado que usa recursos de filtro, o método [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) do alocador deverá conter o bloqueio de streaming, assim como acontece com outros métodos de streaming:


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



