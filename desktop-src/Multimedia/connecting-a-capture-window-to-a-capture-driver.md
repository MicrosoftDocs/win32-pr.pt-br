---
title: Conectando uma janela de captura a um driver de captura
description: Conectando uma janela de captura a um driver de captura
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- WM_CAP_DRIVER_CONNECT mensagem
- macro capDriverConnect
- função capGetDriverDescription
- WM_CAP_DRIVER_GET_NAME mensagem
- macro capDriverGetName
- WM_CAP_DRIVER_GET_VERSION mensagem
- macro capDriverGetVersion
- WM_CAP_DRIVER_DISCONNECT mensagem
- macro capDriverDisconnect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635787"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="1c47e-112">Conectando uma janela de captura a um driver de captura</span><span class="sxs-lookup"><span data-stu-id="1c47e-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="1c47e-113">Você pode conectar ou desconectar dinamicamente uma janela de captura a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="1c47e-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="1c47e-114">Você pode conectar ou associar uma janela de captura a um driver de captura usando a mensagem de [**conexão do driver do WM \_ \_ \_ Cap**](wm-cap-driver-connect.md) (ou a macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ).</span><span class="sxs-lookup"><span data-stu-id="1c47e-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="1c47e-115">Depois que uma janela de captura e o driver de captura estiverem conectados, você poderá enviar mensagens específicas do dispositivo para o driver de captura associado a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="1c47e-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="1c47e-116">Se você tiver mais de um dispositivo de captura instalado em um sistema, poderá conectar uma janela de captura a um driver de dispositivo de captura de vídeo específico especificando um inteiro para o parâmetro *wParam* da mensagem de conexão do driver do WM \_ Cap \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1c47e-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="1c47e-117">O inteiro é um índice que identifica um driver de captura de vídeo listado no registro ou na \[ \] seção de drivers do arquivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="1c47e-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="1c47e-118">Use zero para a primeira entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="1c47e-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="1c47e-119">Você pode recuperar o nome e a versão de um driver de captura instalado usando a função [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) .</span><span class="sxs-lookup"><span data-stu-id="1c47e-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="1c47e-120">Seu aplicativo pode usar essa função para enumerar os dispositivos e drivers de captura instalados, para que o usuário possa selecionar um dispositivo de captura para se conectar a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="1c47e-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="1c47e-121">Você pode recuperar o nome do driver de dispositivo de captura conectado a uma janela de captura usando a mensagem de [**\_ \_ \_ \_ nome Get do driver do WM Cap**](wm-cap-driver-get-name.md) (ou a macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ).</span><span class="sxs-lookup"><span data-stu-id="1c47e-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="1c47e-122">Para recuperar a versão de um driver de captura instalado, use a mensagem [**\_ \_ \_ obter \_ versão do driver do WM Cap**](wm-cap-driver-get-version.md) (ou a macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).</span><span class="sxs-lookup"><span data-stu-id="1c47e-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="1c47e-123">Você pode desconectar uma janela de captura de um driver de captura usando a mensagem de [**\_ \_ \_ desconexão do driver do WM Cap**](wm-cap-driver-disconnect.md) (ou a macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).</span><span class="sxs-lookup"><span data-stu-id="1c47e-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="1c47e-124">Quando uma janela de captura é destruída, todos os drivers de dispositivo de captura de vídeo conectados são desconectados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1c47e-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




