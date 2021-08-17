---
title: Adicionando uma parte de informações
description: Adicionando uma parte de informações
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- Macro capFileSetInfoChunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420181fd0da326ebf3ccc6f921e55161c2005d17c3f8713cd104481147b40f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145129"
---
# <a name="adding-an-information-chunk"></a>Adicionando uma parte de informações

Se você precisar incluir outras informações em seu aplicativo além de áudio e vídeo, poderá criar partes de informações e inseri-las em um arquivo de captura. Partes de informações podem conter vários tipos de informações, incluindo os detalhes de uma notificação de direitos autorais, identificação da fonte do vídeo ou informações de tempo externo. O exemplo a seguir armazena informações de tempo externos um código de tempo SMPTE (Society of Motion Picture and Tv Engineers) em uma parte de informações e adiciona a parte a um arquivo de captura usando a [**macro capFileSetInfoChunk.**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk)


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a Captura de Vídeo](using-video-capture.md)
</dt> </dl>

 

 




