---
title: Captura de User-Initiated
description: Captura de User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822872"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="624e5-105">Captura de User-Initiated</span><span class="sxs-lookup"><span data-stu-id="624e5-105">User-Initiated Capture</span></span>

<span data-ttu-id="624e5-106">Você pode recuperar o valor atual do sinalizador de captura iniciado pelo usuário usando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="624e5-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="624e5-107">O valor do sinalizador é armazenado no membro **fMakeUserHitOKToCapture** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="624e5-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="624e5-108">Você pode fornecer ao usuário um controle preciso sobre quando iniciar uma sessão de captura definindo esse membro como **true**.</span><span class="sxs-lookup"><span data-stu-id="624e5-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="624e5-109">AVICap exibe uma caixa de diálogo depois de alocar todos os buffers de áudio e vídeo para uma sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="624e5-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="624e5-110">Isso permite que o usuário elimine os atrasos de captura devido à inicialização do software.</span><span class="sxs-lookup"><span data-stu-id="624e5-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="624e5-111">Se seu aplicativo usar um pequeno número de buffers de vídeo, essa caixa de diálogo provavelmente será desnecessária.</span><span class="sxs-lookup"><span data-stu-id="624e5-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="624e5-112">O valor padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="624e5-112">The default value is **FALSE**.</span></span>

 

 




