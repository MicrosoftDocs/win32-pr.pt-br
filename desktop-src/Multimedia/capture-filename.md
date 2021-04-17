---
title: Nome do arquivo de captura
description: Nome do arquivo de captura
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE mensagem
- macro capFileSetCaptureFile
- WM_CAP_FILE_GET_CAPTURE_FILE mensagem
- macro capFileGetCaptureFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782314"
---
# <a name="capture-filename"></a><span data-ttu-id="7080e-107">Nome do arquivo de captura</span><span class="sxs-lookup"><span data-stu-id="7080e-107">Capture Filename</span></span>

<span data-ttu-id="7080e-108">O AVICap, por padrão, roteia dados de fluxo de vídeo e áudio de uma janela de captura para um arquivo chamado CAPTURE.AVI no diretório raiz da unidade atual.</span><span class="sxs-lookup"><span data-stu-id="7080e-108">AVICap, by default, routes video and audio stream data from a capture window to a file named CAPTURE.AVI in the root directory of the current drive.</span></span> <span data-ttu-id="7080e-109">Você pode especificar um nome de arquivo alternativo enviando a mensagem do [**arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_**](wm-cap-file-set-capture-file.md) (ou a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7080e-109">You can specify an alternate filename by sending the [**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**](wm-cap-file-set-capture-file.md) message (or the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro) to a capture window.</span></span> <span data-ttu-id="7080e-110">Essa mensagem Especifica o nome do arquivo; Ele não cria, aloca ou abre o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7080e-110">This message specifies the filename; it does not create, allocate, or open the file.</span></span> <span data-ttu-id="7080e-111">Você pode recuperar o nome de arquivo de captura atual enviando a mensagem do [**\_ \_ \_ \_ \_ arquivo de captura do arquivo do WM Cap**](wm-cap-file-get-capture-file.md) (ou a macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="7080e-111">You can retrieve the current capture filename by sending the [**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**](wm-cap-file-get-capture-file.md) message (or the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro) to a capture window.</span></span>

 

 




