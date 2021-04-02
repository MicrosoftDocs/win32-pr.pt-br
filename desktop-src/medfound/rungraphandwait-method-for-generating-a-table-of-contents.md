---
description: Função RunGraphAndWait para gerar um sumário
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Função RunGraphAndWait para gerar um sumário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164889"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a><span data-ttu-id="6ee01-103">Função RunGraphAndWait para gerar um sumário</span><span class="sxs-lookup"><span data-stu-id="6ee01-103">RunGraphAndWait Function for Generating a Table of Contents</span></span>

<span data-ttu-id="6ee01-104">A função a seguir é uma função auxiliar em um programa de exemplo que é abordada na [geração automática de um](generating-a-table-of-contents-automatically.md)Sumário.</span><span class="sxs-lookup"><span data-stu-id="6ee01-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6ee01-105">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ee01-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ee01-106">Gerando um sumário automaticamente</span><span class="sxs-lookup"><span data-stu-id="6ee01-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



