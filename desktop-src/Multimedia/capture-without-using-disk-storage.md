---
title: Capturar sem usar Armazenamento em Disco
description: Capturar sem usar Armazenamento em Disco
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE mensagem
- macro capCaptureSequenceNoFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105752628"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="2c5d7-105">Capturar sem usar Armazenamento em Disco</span><span class="sxs-lookup"><span data-stu-id="2c5d7-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="2c5d7-106">Você pode usar os serviços de captura sem gravar os dados em um arquivo de disco usando a mensagem [**\_ \_ \_ nofile da sequência do WM Cap**](wm-cap-sequence-nofile.md) (ou a macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ).</span><span class="sxs-lookup"><span data-stu-id="2c5d7-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="2c5d7-107">Essa mensagem é útil somente em conjunto com funções de retorno de chamada que permitem que seu aplicativo use os dados de vídeo e áudio diretamente.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="2c5d7-108">Por exemplo, aplicativos de videoconferência podem usar essa mensagem para obter quadros de vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="2c5d7-109">As funções de retorno de chamada transferirão as imagens capturadas para o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="2c5d7-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




