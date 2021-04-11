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
# <a name="adding-an-information-chunk"></a><span data-ttu-id="673c3-104">Adicionando uma parte de informações</span><span class="sxs-lookup"><span data-stu-id="673c3-104">Adding an Information Chunk</span></span>

<span data-ttu-id="673c3-105">Se precisar incluir outras informações em seu aplicativo além de áudio e vídeo, você poderá criar partes de informações e inseri-las em um arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="673c3-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="673c3-106">As partes de informações podem conter vários tipos de informações, incluindo os detalhes de um aviso de direitos autorais, identificação da fonte de vídeo ou informações de tempo externas.</span><span class="sxs-lookup"><span data-stu-id="673c3-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="673c3-107">O exemplo a seguir armazena informações de tempo externas em um código SMPTE (sociedade de imagem de movimento e engenheiros de televisão) em uma parte de informações e adiciona a parte a um arquivo de captura usando a macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="673c3-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="673c3-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="673c3-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="673c3-109">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="673c3-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




