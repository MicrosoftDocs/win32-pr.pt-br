---
title: Capturando dados
description: Capturando dados
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- macro capCaptureSequence
- macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005872"
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

 

 




