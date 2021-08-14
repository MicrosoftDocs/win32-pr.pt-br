---
title: Abrindo um arquivo AVI
description: Abrindo um arquivo AVI
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- Função AVIFileInit
- Função AVIFileOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e8415e6cb3f54dc4eb6bffa11d7f70879546ff2a434fc75cbb91d283bb65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373255"
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



 

 




