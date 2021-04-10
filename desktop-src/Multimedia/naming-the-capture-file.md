---
title: Nomeando o arquivo de captura
description: Nomeando o arquivo de captura
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- macro capFileSetCaptureFile
- macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292361"
---
# <a name="naming-the-capture-file"></a><span data-ttu-id="dcd26-105">Nomeando o arquivo de captura</span><span class="sxs-lookup"><span data-stu-id="dcd26-105">Naming the Capture File</span></span>

<span data-ttu-id="dcd26-106">O exemplo a seguir usa a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) para especificar um nome de arquivo alternativo (MYCAP.AVI) para o arquivo de captura e a macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) para prealocar um arquivo de 5 MB.</span><span class="sxs-lookup"><span data-stu-id="dcd26-106">The following example uses the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro to specify an alternate filename (MYCAP.AVI) for the capture file and the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro to preallocate a file of 5 MB.</span></span>


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="dcd26-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcd26-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcd26-108">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="dcd26-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




