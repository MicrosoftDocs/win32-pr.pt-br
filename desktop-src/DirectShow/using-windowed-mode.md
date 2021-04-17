---
description: Usando o modo de janela
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Usando o modo de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783316"
---
# <a name="using-windowed-mode"></a><span data-ttu-id="21e1b-103">Usando o modo de janela</span><span class="sxs-lookup"><span data-stu-id="21e1b-103">Using Windowed Mode</span></span>

> [!Note]  
> <span data-ttu-id="21e1b-104">O [filtro de processamento de vídeo](video-renderer-filter.md) herdado sempre usa o modo de janela.</span><span class="sxs-lookup"><span data-stu-id="21e1b-104">The legacy [Video Renderer Filter](video-renderer-filter.md) always uses windowed mode.</span></span> <span data-ttu-id="21e1b-105">Os filtros do VMR-7 e do VMR-9 usam o modo de janela por padrão, mas também dão suporte ao modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="21e1b-105">The VMR-7 and VMR-9 filters use windowed mode by default, but also support windowless mode.</span></span>

 

<span data-ttu-id="21e1b-106">No modo de janela, o processador de vídeo cria sua própria janela onde pinta os quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-106">In windowed mode, the video renderer creates its own window where it paints the video frames.</span></span> <span data-ttu-id="21e1b-107">A menos que você especifique o contrário, essa janela é uma janela de nível superior com suas próprias bordas e barra de título.</span><span class="sxs-lookup"><span data-stu-id="21e1b-107">Unless you specify otherwise, this window is a top-level window with its own borders and title bar.</span></span> <span data-ttu-id="21e1b-108">Na maioria das vezes, no entanto, você anexará a janela de vídeo a uma janela de aplicativo, para que o vídeo seja integrado à interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-108">Most of the time, however, you will attach the video window to an application window, so that the video is integrated into your application UI.</span></span> <span data-ttu-id="21e1b-109">Isso exige as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="21e1b-109">This requires the following steps:</span></span>

1.  <span data-ttu-id="21e1b-110">Consulta para **IVideoWindow**.</span><span class="sxs-lookup"><span data-stu-id="21e1b-110">Query for **IVideoWindow**.</span></span>
2.  <span data-ttu-id="21e1b-111">Defina a janela pai.</span><span class="sxs-lookup"><span data-stu-id="21e1b-111">Set the parent window.</span></span>
3.  <span data-ttu-id="21e1b-112">Defina novos estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="21e1b-112">Set new window styles.</span></span>
4.  <span data-ttu-id="21e1b-113">Posicione a janela de vídeo dentro da janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="21e1b-113">Position the video window inside the owner window.</span></span>
5.  <span data-ttu-id="21e1b-114">Notifique a janela de vídeo do WM \_ mover mensagens.</span><span class="sxs-lookup"><span data-stu-id="21e1b-114">Notify the video window of WM\_MOVE messages.</span></span>

<span data-ttu-id="21e1b-115">**Consulta para IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="21e1b-115">**Query for IVideoWindow**</span></span>

<span data-ttu-id="21e1b-116">Antes de iniciar a reprodução, consulte o Gerenciador de gráficos de filtro para a interface **IVideoWindow** :</span><span class="sxs-lookup"><span data-stu-id="21e1b-116">Before starting playback, query the Filter Graph Manager for the **IVideoWindow** interface:</span></span>


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



<span data-ttu-id="21e1b-117">**Definir a janela pai**</span><span class="sxs-lookup"><span data-stu-id="21e1b-117">**Set the Parent Window**</span></span>

<span data-ttu-id="21e1b-118">Para definir a janela pai, chame o método [**IVideoWindow::p UT \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) com um identificador para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-118">To set the parent window, call the [**IVideoWindow::put\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) method with a handle to your application window.</span></span> <span data-ttu-id="21e1b-119">Esse método usa uma variável do tipo [**OAHWND**](oahwnd.md), portanto, converta o identificador para esse tipo:</span><span class="sxs-lookup"><span data-stu-id="21e1b-119">This method takes a variable of type [**OAHWND**](oahwnd.md), so cast the handle to this type:</span></span>


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



<span data-ttu-id="21e1b-120">**Definir novos estilos de janela**</span><span class="sxs-lookup"><span data-stu-id="21e1b-120">**Set New Window Styles**</span></span>

<span data-ttu-id="21e1b-121">Altere o estilo da janela de vídeo chamando o método [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :</span><span class="sxs-lookup"><span data-stu-id="21e1b-121">Change the style of the video window by calling the [**IVideoWindow::put\_WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) method:</span></span>


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



<span data-ttu-id="21e1b-122">O \_ sinalizador WS Child define a janela como uma janela filho, e o sinalizador WS \_ CLIPSIBLINGS impede que a janela seja desenhada dentro da área do cliente de outra janela filho.</span><span class="sxs-lookup"><span data-stu-id="21e1b-122">The WS\_CHILD flag sets the window to be a child window, and the WS\_CLIPSIBLINGS flag prevents the window from drawing inside the client area of another child window.</span></span>

<span data-ttu-id="21e1b-123">**Posicionar a janela de vídeo**</span><span class="sxs-lookup"><span data-stu-id="21e1b-123">**Position the Video Window**</span></span>

<span data-ttu-id="21e1b-124">Para definir a posição do vídeo em relação à área do cliente da janela do aplicativo, chame o método [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="21e1b-124">To set the position of the video relative to the application window's client area, call the [**IVideoWindow::SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) method.</span></span> <span data-ttu-id="21e1b-125">Esse método usa um retângulo que especifica a borda esquerda, a borda superior, a largura e a altura da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-125">This method takes a rectangle that specifies the left edge, top edge, width, and height of the video window.</span></span> <span data-ttu-id="21e1b-126">Por exemplo, o código a seguir estica a janela de vídeo para se ajustar a toda a área do cliente da janela pai:</span><span class="sxs-lookup"><span data-stu-id="21e1b-126">For example, the following code stretches the video window to fit the entire client area of the parent window:</span></span>


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



<span data-ttu-id="21e1b-127">Para obter o tamanho nativo do vídeo, chame o método [**IBasicVideo::**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) getplotize no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="21e1b-127">To get the native size of the video, call the [**IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) method on the Filter Graph Manager.</span></span> <span data-ttu-id="21e1b-128">Você pode usar essas informações para dimensionar o vídeo e manter a taxa de proporção correta.</span><span class="sxs-lookup"><span data-stu-id="21e1b-128">You can use that information to scale the video and keep the correct aspect ratio.</span></span>

<span data-ttu-id="21e1b-129">**Responder às mensagens de movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="21e1b-129">**Respond to WM\_MOVE Messages**</span></span>

<span data-ttu-id="21e1b-130">Para obter o melhor desempenho, você deve notificar o renderizador de vídeo sempre que a janela for movida enquanto o grafo estiver em pausa.</span><span class="sxs-lookup"><span data-stu-id="21e1b-130">For best performance, you should notify the video renderer whenever the window moves while the graph is paused.</span></span> <span data-ttu-id="21e1b-131">Chame o método [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para encaminhar a \_ mensagem de movimentação do WM:</span><span class="sxs-lookup"><span data-stu-id="21e1b-131">Call the [**IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) method to forward the WM\_MOVE message:</span></span>


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



<span data-ttu-id="21e1b-132">Se o renderizador estiver usando uma sobreposição de hardware, essa notificação fará com que o renderizador atualize a posição da sobreposição.</span><span class="sxs-lookup"><span data-stu-id="21e1b-132">If the renderer is using a hardware overlay, this notification causes the renderer to update the overlay position.</span></span> <span data-ttu-id="21e1b-133">(O VMR-9 não usa sobreposições, portanto, você não precisa chamar esse método se estiver usando o VMR-9.)</span><span class="sxs-lookup"><span data-stu-id="21e1b-133">(The VMR-9 does not use overlays, so you do not need to call this method if you are using the VMR-9.)</span></span>

<span data-ttu-id="21e1b-134">**Limpar**</span><span class="sxs-lookup"><span data-stu-id="21e1b-134">**Clean Up**</span></span>

<span data-ttu-id="21e1b-135">Antes de o aplicativo sair, pare o grafo e redefina o proprietário da janela de vídeo como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="21e1b-135">Before the application exits, stop the graph and reset the video window's owner to **NULL**.</span></span> <span data-ttu-id="21e1b-136">Caso contrário, as mensagens de janela podem ser enviadas para a janela errada, o que provavelmente causará erros.</span><span class="sxs-lookup"><span data-stu-id="21e1b-136">Otherwise, window messages might be sent to the wrong window, which is likely to cause errors.</span></span> <span data-ttu-id="21e1b-137">Além disso, oculte a janela de vídeo ou, caso contrário, você poderá ver uma cintilação de imagem de vídeo na tela momentaneamente:</span><span class="sxs-lookup"><span data-stu-id="21e1b-137">Also, hide video window, or else you might see a video image flicker on the screen momentarily:</span></span>


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> <span data-ttu-id="21e1b-138">Se o pai da janela de vídeo for um filho de sua janela principal do aplicativo (em outras palavras, se a janela de vídeo for um filho de um filho), você deverá criar a janela de vídeo usando **CoCreateInstance** e adicioná-la ao grafo, em vez de permitir que o Gerenciador de gráfico de filtro adicione o renderizador de vídeo durante o [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="21e1b-138">If the parent of the video window is a child of your main application window (in other words, if the video window is a child of a child), you should create the video window using **CoCreateInstance** and add it to the graph, instead of letting the Filter Graph Manager add the video renderer during [Intelligent Connect](intelligent-connect.md).</span></span> <span data-ttu-id="21e1b-139">Isso garante que a janela de vídeo e sua janela filho sejam repintadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-139">This ensures that the video window and your child window are repainted at the same time.</span></span> <span data-ttu-id="21e1b-140">Caso contrário, a janela filho poderá pintar sobre a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="21e1b-140">Otherwise, the child window may paint over the video window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="21e1b-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21e1b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21e1b-142">Renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="21e1b-142">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



