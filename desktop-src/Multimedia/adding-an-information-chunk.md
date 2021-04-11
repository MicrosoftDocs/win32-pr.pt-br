---
title: Adicionando uma parte de informações
description: Adicionando uma parte de informações
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- macro capFileSetInfoChunk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159957"
---
# <a name="adding-an-information-chunk"></a>Adicionando uma parte de informações

Se precisar incluir outras informações em seu aplicativo além de áudio e vídeo, você poderá criar partes de informações e inseri-las em um arquivo de captura. As partes de informações podem conter vários tipos de informações, incluindo os detalhes de um aviso de direitos autorais, identificação da fonte de vídeo ou informações de tempo externas. O exemplo a seguir armazena informações de tempo externas em um código SMPTE (sociedade de imagem de movimento e engenheiros de televisão) em uma parte de informações e adiciona a parte a um arquivo de captura usando a macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


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

[Usando a captura de vídeo](using-video-capture.md)
</dt> </dl>

 

 




