---
title: Abrindo um arquivo AVI
description: Abrindo um arquivo AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- Função AVIFileInit
- Função AVIFileOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833219194dc984bbf7bfa3d0415f77c5eed9b43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453604"
---
# <a name="opening-an-avi-file"></a>Abrindo um arquivo AVI

O exemplo a seguir inicializa a biblioteca AVIFile usando a função [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) e abre um arquivo AVI usando a função [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . A função usa um manipulador de arquivo padrão.


```C++
// LoadAVIFile - loads AVIFile and opens an AVI file. 
// 
// szfile - filename 
// hwnd - window handle 
// 
VOID LoadAVIFile(LPCSTR szFile, HWND hwnd) 
{ 
    LONG hr; 
    PAVIFILE pfile; 
 
    AVIFileInit();          // opens AVIFile library 
 
    hr = AVIFileOpen(&pfile, szFile, OF_SHARE_DENY_WRITE, 0L); 
    if (hr != 0){ 
        // Handle failure.
        return; 
    } 
 
// 
// Place functions here that interact with the open file. 
// 
 
    AVIFileRelease(pfile);  // closes the file 
    AVIFileExit();          // releases AVIFile library 
} 
 
```



 

 




