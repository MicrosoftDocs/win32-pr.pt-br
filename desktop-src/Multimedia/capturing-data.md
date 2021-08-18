---
title: Capturando dados
description: Capturando dados
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- macro capCaptureSequence
- macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764ff00dedcc044ed5234f8b647b08eaded35ce191bcb56e05cb35f47450677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941294"
---
# <a name="capturing-data"></a>Capturando dados

O exemplo a seguir usa a macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) para iniciar a captura de vídeo e a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) para copiar os dados capturados do arquivo de captura para o arquivo NEWFILE.AVI.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




