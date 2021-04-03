---
title: Status da janela de captura
description: Status da janela de captura
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS mensagem
- macro capGetStatus
- Estrutura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005912"
---
# <a name="capture-window-status"></a><span data-ttu-id="bd298-106">Status da janela de captura</span><span class="sxs-lookup"><span data-stu-id="bd298-106">Capture Window Status</span></span>

<span data-ttu-id="bd298-107">Você pode recuperar o status atual de uma janela de captura usando a mensagem de [**\_ \_ \_ status Get do WM Cap**](wm-cap-get-status.md) (ou a macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ).</span><span class="sxs-lookup"><span data-stu-id="bd298-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="bd298-108">Essa mensagem recupera uma cópia da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) com os valores atuais de seus membros.</span><span class="sxs-lookup"><span data-stu-id="bd298-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="bd298-109">A estrutura **CAPSTATUS** contém informações sobre as dimensões da imagem, a posição da rolagem e se a sobreposição ou visualização da imagem está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bd298-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="bd298-110">Como as informações representadas em **CAPSTATUS** são dinâmicas, o aplicativo deve atualizar o conteúdo da estrutura sempre que o tamanho ou o formato do fluxo de vídeo capturado pode ter mudado (como após a exibição do formato de vídeo do driver de captura).</span><span class="sxs-lookup"><span data-stu-id="bd298-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="bd298-111">Alterar as dimensões da janela de captura não tem nenhum efeito sobre as dimensões do fluxo de vídeo capturado real.</span><span class="sxs-lookup"><span data-stu-id="bd298-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="bd298-112">A caixa de diálogo formato exibida pelo driver de dispositivo de captura de vídeo controla as dimensões do fluxo de vídeo capturado.</span><span class="sxs-lookup"><span data-stu-id="bd298-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




