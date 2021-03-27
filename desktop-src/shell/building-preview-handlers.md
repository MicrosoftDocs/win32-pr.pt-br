---
description: Este tópico discute as interfaces e os métodos específicos necessários para criar um Gerenciador de visualização.
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: Criando gerenciadores de visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296219"
---
# <a name="building-preview-handlers"></a><span data-ttu-id="920a5-103">Criando gerenciadores de visualização</span><span class="sxs-lookup"><span data-stu-id="920a5-103">Building Preview Handlers</span></span>

<span data-ttu-id="920a5-104">Este tópico discute as interfaces e os métodos específicos necessários para criar um Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="920a5-104">This topic discusses the specific interfaces and methods required to create a preview handler.</span></span>

<span data-ttu-id="920a5-105">Um Gerenciador de visualização deve implementar as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="920a5-105">A preview handler must implement the following interfaces:</span></span>

-   <span data-ttu-id="920a5-106">[IInitializeWithStream:: Initialize](#iinitializewithstreaminitialize) (altamente preferencial), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)ou [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)</span><span class="sxs-lookup"><span data-stu-id="920a5-106">[IInitializeWithStream::Initialize](#iinitializewithstreaminitialize) (strongly preferred), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile), or [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)</span></span>
-   [<span data-ttu-id="920a5-107">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="920a5-107">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="920a5-108">IOleWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-108">IOleWindow</span></span>](#iolewindow)
-   [<span data-ttu-id="920a5-109">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="920a5-109">IPreviewHandler</span></span>](#ipreviewhandler)

<span data-ttu-id="920a5-110">Se o seu Gerenciador de visualização oferecer suporte a configurações visuais fornecidas pelo host, como cor e fonte do plano de fundo, ele também deverá implementar a seguinte interface:</span><span class="sxs-lookup"><span data-stu-id="920a5-110">If your preview handler supports visual settings provided by the host such as background color and font, it must also implement the following interface:</span></span>

-   [<span data-ttu-id="920a5-111">IPreviewHandlerVisuals</span><span class="sxs-lookup"><span data-stu-id="920a5-111">IPreviewHandlerVisuals</span></span>](#ipreviewhandlervisuals)

<span data-ttu-id="920a5-112">Este tópico pressupõe que o Gerenciador de visualização seja inicializado com um fluxo e seja registrado para uma extensão de nome de arquivo específica.</span><span class="sxs-lookup"><span data-stu-id="920a5-112">This topic assumes that the preview handler is initialized with a stream and is registered for a particular file name extension.</span></span>

## <a name="iinitializewithstreaminitialize"></a><span data-ttu-id="920a5-113">IInitializeWithStream:: Initialize</span><span class="sxs-lookup"><span data-stu-id="920a5-113">IInitializeWithStream::Initialize</span></span>

<span data-ttu-id="920a5-114">Armazene os parâmetros de [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) e de modo para que você possa ler os dados do item quando estiver pronto para visualizar o item.</span><span class="sxs-lookup"><span data-stu-id="920a5-114">Store the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) and mode parameters so that you can read the item's data when you are ready to preview the item.</span></span> <span data-ttu-id="920a5-115">Não carregue os dados na [**inicialização**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize).</span><span class="sxs-lookup"><span data-stu-id="920a5-115">Do not load the data in [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="920a5-116">Carregue os dados em [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) antes de renderizar.</span><span class="sxs-lookup"><span data-stu-id="920a5-116">Load the data in [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) just before you render.</span></span>

## <a name="iobjectwithsite"></a><span data-ttu-id="920a5-117">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="920a5-117">IObjectWithSite</span></span>

-   [<span data-ttu-id="920a5-118">IObjectWithSite:: SetSite</span><span class="sxs-lookup"><span data-stu-id="920a5-118">IObjectWithSite::SetSite</span></span>](#iobjectwithsitesetsite)
-   [<span data-ttu-id="920a5-119">IObjectWithSite:: GetSite</span><span class="sxs-lookup"><span data-stu-id="920a5-119">IObjectWithSite::GetSite</span></span>](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a><span data-ttu-id="920a5-120">IObjectWithSite:: SetSite</span><span class="sxs-lookup"><span data-stu-id="920a5-120">IObjectWithSite::SetSite</span></span>

<span data-ttu-id="920a5-121">Armazene o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para acesso posterior.</span><span class="sxs-lookup"><span data-stu-id="920a5-121">Store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for later access.</span></span>

<span data-ttu-id="920a5-122">Se, no momento, você tiver uma referência a um objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) , libere-o.</span><span class="sxs-lookup"><span data-stu-id="920a5-122">If you currently have a reference to an [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) object, release it.</span></span> <span data-ttu-id="920a5-123">Use o ponteiro de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) armazenado para chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para uma nova referência de **IPreviewHandlerFrame** .</span><span class="sxs-lookup"><span data-stu-id="920a5-123">Use the stored [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for a new **IPreviewHandlerFrame** reference.</span></span>

<span data-ttu-id="920a5-124">Se você tiver uma tabela de acelerador, destrua-a.</span><span class="sxs-lookup"><span data-stu-id="920a5-124">If you currently have an accelerator table, destroy it.</span></span> <span data-ttu-id="920a5-125">Chame [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) para obter uma nova tabela de acelerador.</span><span class="sxs-lookup"><span data-stu-id="920a5-125">Call [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) to get a new accelerator table.</span></span> <span data-ttu-id="920a5-126">Armazene esta tabela.</span><span class="sxs-lookup"><span data-stu-id="920a5-126">Store this table.</span></span> <span data-ttu-id="920a5-127">Observe que ele é usado apenas como uma lista de teclas de aceleração com suporte no quadro.</span><span class="sxs-lookup"><span data-stu-id="920a5-127">Note that it is used only as a list of accelerator keys that the frame supports.</span></span> <span data-ttu-id="920a5-128">Os comandos nas entradas do acelerador são ignorados.</span><span class="sxs-lookup"><span data-stu-id="920a5-128">Commands in the accelerator entries are ignored.</span></span>

### <a name="iobjectwithsitegetsite"></a><span data-ttu-id="920a5-129">IObjectWithSite:: GetSite</span><span class="sxs-lookup"><span data-stu-id="920a5-129">IObjectWithSite::GetSite</span></span>

<span data-ttu-id="920a5-130">Retorne o ponteiro do site, seja qual for.</span><span class="sxs-lookup"><span data-stu-id="920a5-130">Return the site pointer, whatever it is.</span></span>

## <a name="iolewindow"></a><span data-ttu-id="920a5-131">IOleWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-131">IOleWindow</span></span>

-   [<span data-ttu-id="920a5-132">IOleWindow::ContextSensitiveHelp</span><span class="sxs-lookup"><span data-stu-id="920a5-132">IOleWindow::ContextSensitiveHelp</span></span>](#iolewindowcontextsensitivehelp)
-   [<span data-ttu-id="920a5-133">IOleWindow:: GetWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-133">IOleWindow::GetWindow</span></span>](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a><span data-ttu-id="920a5-134">IOleWindow::ContextSensitiveHelp</span><span class="sxs-lookup"><span data-stu-id="920a5-134">IOleWindow::ContextSensitiveHelp</span></span>

<span data-ttu-id="920a5-135">Retornar E \_ NOTIMPL para este método.</span><span class="sxs-lookup"><span data-stu-id="920a5-135">Return E\_NOTIMPL for this method.</span></span>

### <a name="iolewindowgetwindow"></a><span data-ttu-id="920a5-136">IOleWindow:: GetWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-136">IOleWindow::GetWindow</span></span>

<span data-ttu-id="920a5-137">Se a janela do Gerenciador de visualização existir no momento, retorne o **HWND** dessa janela e s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="920a5-137">If the preview handler's window currently exists, return the **HWND** of that window and S\_OK.</span></span> <span data-ttu-id="920a5-138">Se a janela não existir, retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="920a5-138">If the window does not exist, return E\_FAIL.</span></span>

## <a name="ipreviewhandler"></a><span data-ttu-id="920a5-139">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="920a5-139">IPreviewHandler</span></span>

-   [<span data-ttu-id="920a5-140">IPreviewHandler:: SetWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-140">IPreviewHandler::SetWindow</span></span>](#ipreviewhandlersetwindow)
-   [<span data-ttu-id="920a5-141">IPreviewHandler:: SetRect</span><span class="sxs-lookup"><span data-stu-id="920a5-141">IPreviewHandler::SetRect</span></span>](#ipreviewhandlersetrect)
-   [<span data-ttu-id="920a5-142">IPreviewHandler::D oPreview</span><span class="sxs-lookup"><span data-stu-id="920a5-142">IPreviewHandler::DoPreview</span></span>](#ipreviewhandlerdopreview)
-   [<span data-ttu-id="920a5-143">IPreviewHandler:: SetFocus</span><span class="sxs-lookup"><span data-stu-id="920a5-143">IPreviewHandler::SetFocus</span></span>](#ipreviewhandlersetfocus)
-   [<span data-ttu-id="920a5-144">IPreviewHandler:: QueryFocus</span><span class="sxs-lookup"><span data-stu-id="920a5-144">IPreviewHandler::QueryFocus</span></span>](#ipreviewhandlerqueryfocus)
-   [<span data-ttu-id="920a5-145">IPreviewHandler:: TranslateAccelerator</span><span class="sxs-lookup"><span data-stu-id="920a5-145">IPreviewHandler::TranslateAccelerator</span></span>](#ipreviewhandlertranslateaccelerator)
-   [<span data-ttu-id="920a5-146">IPreviewHandler:: Unload</span><span class="sxs-lookup"><span data-stu-id="920a5-146">IPreviewHandler::Unload</span></span>](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a><span data-ttu-id="920a5-147">IPreviewHandler:: SetWindow</span><span class="sxs-lookup"><span data-stu-id="920a5-147">IPreviewHandler::SetWindow</span></span>

<span data-ttu-id="920a5-148">Defina o parâmetro *HWND* deste método como o pai do **HWND** do Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="920a5-148">Set the *hwnd* parameter of this method to the parent of your preview handler's **HWND**.</span></span> <span data-ttu-id="920a5-149">Esse método pode ser chamado várias vezes.</span><span class="sxs-lookup"><span data-stu-id="920a5-149">This method can be called multiple times.</span></span> <span data-ttu-id="920a5-150">Redimensione sua visualização para que ela seja renderizada apenas na área descrita pelo parâmetro *prc* .</span><span class="sxs-lookup"><span data-stu-id="920a5-150">Resize your preview so that it renders only in the area described by the *prc* parameter.</span></span>

<span data-ttu-id="920a5-151">Se o previsor estiver no processo de renderização, use o método [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) para alterar o pai do pré-visor.</span><span class="sxs-lookup"><span data-stu-id="920a5-151">If the previewer is in the process of rendering, use the [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) method to change the parent of the previewer.</span></span> <span data-ttu-id="920a5-152">Altere também a área na qual o previsor está renderizando.</span><span class="sxs-lookup"><span data-stu-id="920a5-152">Also change the area in which the previewer is rendering.</span></span>

### <a name="ipreviewhandlersetrect"></a><span data-ttu-id="920a5-153">IPreviewHandler:: SetRect</span><span class="sxs-lookup"><span data-stu-id="920a5-153">IPreviewHandler::SetRect</span></span>

<span data-ttu-id="920a5-154">Redimensione sua visualização para que ela seja renderizada apenas na área descrita pelo *prc* desse método.</span><span class="sxs-lookup"><span data-stu-id="920a5-154">Resize your preview so that it only renders in the area described by this method's *prc*.</span></span>

<span data-ttu-id="920a5-155">Se o previsor estiver no processo de renderização, altere a área em que o seu visualizador é renderizado.</span><span class="sxs-lookup"><span data-stu-id="920a5-155">If the previewer is in the process of rendering, change the area in which your previewer renders.</span></span>

### <a name="ipreviewhandlerdopreview"></a><span data-ttu-id="920a5-156">IPreviewHandler::D oPreview</span><span class="sxs-lookup"><span data-stu-id="920a5-156">IPreviewHandler::DoPreview</span></span>

<span data-ttu-id="920a5-157">É aí que o trabalho real é feito.</span><span class="sxs-lookup"><span data-stu-id="920a5-157">This is where the real work is done.</span></span> <span data-ttu-id="920a5-158">Como uma visualização é dinâmica, o conteúdo da visualização só deve ser carregado quando necessário.</span><span class="sxs-lookup"><span data-stu-id="920a5-158">Since a preview is dynamic, the preview content should only be loaded when it is needed.</span></span> <span data-ttu-id="920a5-159">Não carregue o conteúdo na inicialização.</span><span class="sxs-lookup"><span data-stu-id="920a5-159">Do not load content in the initialization.</span></span>

<span data-ttu-id="920a5-160">Se a janela do Gerenciador de visualização não existir, crie-a.</span><span class="sxs-lookup"><span data-stu-id="920a5-160">If the preview handler window does not exist, create it.</span></span> <span data-ttu-id="920a5-161">As janelas do Gerenciador de visualização devem ser filhas da janela fornecida por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).</span><span class="sxs-lookup"><span data-stu-id="920a5-161">Your preview handler's windows should be children of the window provided by [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).</span></span> <span data-ttu-id="920a5-162">Eles devem ter o tamanho fornecido por **IPreviewHandler:: SetWindow** e [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (o que foi chamado mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="920a5-162">They should be the size provided by **IPreviewHandler::SetWindow** and [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (whichever was called most recently).</span></span>

<span data-ttu-id="920a5-163">Quando você tiver uma janela, carregue os dados do [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) com o qual o Gerenciador de visualização foi inicializado e os processe para a janela do seu Gerenciador de visualização.</span><span class="sxs-lookup"><span data-stu-id="920a5-163">Once you have a window, load the data from the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that the preview handler was initialized with, and render that data to your preview handler's window.</span></span>

### <a name="ipreviewhandlersetfocus"></a><span data-ttu-id="920a5-164">IPreviewHandler:: SetFocus</span><span class="sxs-lookup"><span data-stu-id="920a5-164">IPreviewHandler::SetFocus</span></span>

<span data-ttu-id="920a5-165">Esse método é chamado quando o foco entra no painel de leitura por meio de uma ação de guia.</span><span class="sxs-lookup"><span data-stu-id="920a5-165">This method is called when the focus enters the reading pane through a tab action.</span></span> <span data-ttu-id="920a5-166">Como ele pode ser inserido como uma guia avançar ou uma guia reversa, use o estado atual da tecla SHIFT para decidir se a primeira ou última parada de tabulação no painel de leitura deve receber o foco.</span><span class="sxs-lookup"><span data-stu-id="920a5-166">Since it can be entered as a forward tab or reverse tab, use the current state of the SHIFT key to decide whether the first or last tab stop in the reading pane should receive the focus.</span></span>

### <a name="ipreviewhandlerqueryfocus"></a><span data-ttu-id="920a5-167">IPreviewHandler:: QueryFocus</span><span class="sxs-lookup"><span data-stu-id="920a5-167">IPreviewHandler::QueryFocus</span></span>

<span data-ttu-id="920a5-168">Esse método deve chamar a função [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) e retornar o resultado dessa chamada no parâmetro *phwnd* .</span><span class="sxs-lookup"><span data-stu-id="920a5-168">This method should call the [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) function and return the result of that call in the *phwnd* parameter.</span></span>

### <a name="ipreviewhandlertranslateaccelerator"></a><span data-ttu-id="920a5-169">IPreviewHandler:: TranslateAccelerator</span><span class="sxs-lookup"><span data-stu-id="920a5-169">IPreviewHandler::TranslateAccelerator</span></span>

<span data-ttu-id="920a5-170">Esse método é chamado pelo bombeamento da mensagem do processo do Gerenciador de visualização (se prevhost.exe ou um servidor local personalizado) em resposta a pressionamentos de tecla do usuário.</span><span class="sxs-lookup"><span data-stu-id="920a5-170">This method is called by the message pump of the preview handler's process (whether prevhost.exe or a custom local server) in response to user keystrokes.</span></span> <span data-ttu-id="920a5-171">Os gerenciadores de visualização devem lidar com esses pressionamentos de teclas ou encaminhá-los ao host de acordo com o algoritmo detalhado abaixo.</span><span class="sxs-lookup"><span data-stu-id="920a5-171">Preview handlers should handle these keystrokes or forward them to their host according to the algorithm detailed below.</span></span>

<span data-ttu-id="920a5-172">No entanto, como as visualizações são somente leitura, a entrada do teclado deve ser mínima e otimizações como essa não são necessárias em muitos casos.</span><span class="sxs-lookup"><span data-stu-id="920a5-172">However, because previews are read-only, keyboard input should be minimal and optimizations such as this are not needed in many cases.</span></span>

<span data-ttu-id="920a5-173">Se o acelerador de teclado passado para esse método por meio da bomba de mensagem for um acelerador que o seu Gerenciador de visualização aceitará, processe-o e retorne os S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="920a5-173">If the keyboard accelerator passed to this method through the message pump is an accelerator that your preview handler accepts, then process it and return S\_OK.</span></span> <span data-ttu-id="920a5-174">Se o manipulador não aceitar esse acelerador, a mensagem do acelerador poderá ser enviada de volta até o quadro a ser manipulado.</span><span class="sxs-lookup"><span data-stu-id="920a5-174">If your handler does not accept that accelerator, the accelerator message can be sent back as far as the frame to be handled.</span></span>

<span data-ttu-id="920a5-175">Há duas opções para encaminhar aceleradores de teclado de volta ao quadro:</span><span class="sxs-lookup"><span data-stu-id="920a5-175">There are two options for forwarding keyboard accelerators back to the frame:</span></span>

<span data-ttu-id="920a5-176">O modelo mais simples é encaminhar todos os pressionamentos de tecla para o host usando [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="920a5-176">The simplest model is to forward all keystrokes to the host using [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator).</span></span> <span data-ttu-id="920a5-177">Isso é feito no exemplo do Gerenciador de visualização fornecido com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="920a5-177">This is done in the preview handler sample provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="920a5-178">Todos os gerenciadores de visualização de baixa integridade devem usar esse modelo.</span><span class="sxs-lookup"><span data-stu-id="920a5-178">All low-integrity preview handlers must use this model.</span></span> <span data-ttu-id="920a5-179">Se o acelerador não for tratado pelo seu Gerenciador de visualização, chame **IPreviewHandlerFrame:: TranslateAccelerator** e retorne seu resultado.</span><span class="sxs-lookup"><span data-stu-id="920a5-179">If the accelerator is not handled by your preview handler, call **IPreviewHandlerFrame::TranslateAccelerator** and return its result.</span></span>

<span data-ttu-id="920a5-180">O outro modelo é usar uma tabela de acelerador como uma otimização para evitar o envio de muitos pressionamentos de tecla entre limites de processo:</span><span class="sxs-lookup"><span data-stu-id="920a5-180">The other model is to use an accelerator table as an optimization to avoid sending too many keystrokes across process boundaries:</span></span>

1.  <span data-ttu-id="920a5-181">Quando [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) é chamado no seu Gerenciador de visualização, adquira a tabela de acelerador por meio de [**IPreviewHandlerFrame:: GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext).</span><span class="sxs-lookup"><span data-stu-id="920a5-181">When [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is called on your preview handler, acquire the accelerator table through [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext).</span></span> <span data-ttu-id="920a5-182">(Certifique-se de liberar o identificador para a tabela de aceleração quando o seu visualizador for destruído.)</span><span class="sxs-lookup"><span data-stu-id="920a5-182">(Be sure to free the handle to the accelerator table when your previewer is destroyed.)</span></span>
2.  <span data-ttu-id="920a5-183">Se o acelerador for manipulado pelo seu Gerenciador de visualização, manipule-o e retorne os S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="920a5-183">If the accelerator is handled by your preview handler, handle it and return S\_OK.</span></span>
3.  <span data-ttu-id="920a5-184">Se o acelerador não for manipulado pelo seu Gerenciador de visualização, compare a mensagem usando [**isaccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) com base na tabela de aceleração adquirida.</span><span class="sxs-lookup"><span data-stu-id="920a5-184">If the accelerator is not handled by your preview handler, compare the message using [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) against the accelerator table acquired.</span></span>
4.  <span data-ttu-id="920a5-185">Se o acelerador corresponder a uma entrada nessa tabela de acelerador, chame [**IPreviewHandlerFrame:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) e retorne seu resultado.</span><span class="sxs-lookup"><span data-stu-id="920a5-185">If the accelerator matches an entry in that accelerator table, call [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) and return its result.</span></span>
5.  <span data-ttu-id="920a5-186">Se o acelerador não corresponder a nenhuma entrada na tabela do acelerador, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="920a5-186">If the accelerator does not match any entry in the accelerator table, return S\_FALSE.</span></span>

### <a name="ipreviewhandlerunload"></a><span data-ttu-id="920a5-187">IPreviewHandler:: Unload</span><span class="sxs-lookup"><span data-stu-id="920a5-187">IPreviewHandler::Unload</span></span>

<span data-ttu-id="920a5-188">Quando esse método é chamado, pare qualquer renderização, libere todos os recursos alocados lendo dados do fluxo e libere o [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) em si.</span><span class="sxs-lookup"><span data-stu-id="920a5-188">When this method is called, stop any rendering, release any resources allocated by reading data from the stream, and release the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) itself.</span></span>

<span data-ttu-id="920a5-189">Depois que esse método é chamado, o manipulador deve ser reinicializado antes de qualquer tentativa de chamar [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) novamente.</span><span class="sxs-lookup"><span data-stu-id="920a5-189">Once this method is called, the handler must be reinitialized before any attempt to call [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) again.</span></span>

## <a name="ipreviewhandlervisuals"></a><span data-ttu-id="920a5-190">IPreviewHandlerVisuals</span><span class="sxs-lookup"><span data-stu-id="920a5-190">IPreviewHandlerVisuals</span></span>

-   [<span data-ttu-id="920a5-191">IPreviewHandlerVisuals:: setBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="920a5-191">IPreviewHandlerVisuals::SetBackgroundColor</span></span>](#ipreviewhandlervisualssetbackgroundcolor)
-   [<span data-ttu-id="920a5-192">IPreviewHandlerVisuals:: SetFont</span><span class="sxs-lookup"><span data-stu-id="920a5-192">IPreviewHandlerVisuals::SetFont</span></span>](#ipreviewhandlervisualssetfont)
-   [<span data-ttu-id="920a5-193">IPreviewHandlerVisuals::SetTextColor</span><span class="sxs-lookup"><span data-stu-id="920a5-193">IPreviewHandlerVisuals::SetTextColor</span></span>](#ipreviewhandlervisualssettextcolor)

<span data-ttu-id="920a5-194">Esses métodos devem ser implementados ao direcionar o Gerenciador de visualização para responder aos esquemas de cores e fontes do host.</span><span class="sxs-lookup"><span data-stu-id="920a5-194">These methods should be implemented when directing the preview handler to respond to the host's color and font schemes.</span></span> <span data-ttu-id="920a5-195">O host consulta o manipulador para [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals).</span><span class="sxs-lookup"><span data-stu-id="920a5-195">The host queries the handler for [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals).</span></span> <span data-ttu-id="920a5-196">Se houver suporte, o host o fornecerá com cores, fontes e cor do texto.</span><span class="sxs-lookup"><span data-stu-id="920a5-196">If found to be supported, the host provides it with color, font, and text color.</span></span>

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a><span data-ttu-id="920a5-197">IPreviewHandlerVisuals:: setBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="920a5-197">IPreviewHandlerVisuals::SetBackgroundColor</span></span>

<span data-ttu-id="920a5-198">Armazene essa cor e use-a durante a renderização quando desejar fornecer uma cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="920a5-198">Store this color and use it during rendering when you want to provide a background color.</span></span> <span data-ttu-id="920a5-199">Por exemplo, para preencher a janela quando o manipulador é renderizado para uma área menor do que a área fornecida por [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) e [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).</span><span class="sxs-lookup"><span data-stu-id="920a5-199">For instance, to fill the window when the handler renders to an area smaller than the area provided by [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) and [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).</span></span> <span data-ttu-id="920a5-200">Observe, no entanto, que você não deve desenhar fora da área fornecida por esses métodos.</span><span class="sxs-lookup"><span data-stu-id="920a5-200">Note, however, that you should not draw outside the area provided by those methods.</span></span>

<span data-ttu-id="920a5-201">Se esse método for chamado enquanto a visualização já estiver sendo processada, a renderização deverá ser reiniciada usando essa cor de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="920a5-201">If this method is called while the preview is already being rendered, the rendering should be restarted using this background color.</span></span>

### <a name="ipreviewhandlervisualssetfont"></a><span data-ttu-id="920a5-202">IPreviewHandlerVisuals:: SetFont</span><span class="sxs-lookup"><span data-stu-id="920a5-202">IPreviewHandlerVisuals::SetFont</span></span>

<span data-ttu-id="920a5-203">Armazene essas informações de fonte e use-as durante a renderização quando desejar exibir texto consistente com as configurações atuais do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="920a5-203">Store this font information and use it during rendering when you want to display text consistent with the current Windows Vista settings.</span></span>

### <a name="ipreviewhandlervisualssettextcolor"></a><span data-ttu-id="920a5-204">IPreviewHandlerVisuals::SetTextColor</span><span class="sxs-lookup"><span data-stu-id="920a5-204">IPreviewHandlerVisuals::SetTextColor</span></span>

<span data-ttu-id="920a5-205">Armazene essas informações de cor do texto e use-as durante a renderização quando desejar exibir texto consistente com as configurações atuais do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="920a5-205">Store this text color information and use it during rendering when you want to display text consistent with the current Windows Vista settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="920a5-206">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="920a5-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920a5-207">Gerenciadores de visualização e host de visualização do Shell</span><span class="sxs-lookup"><span data-stu-id="920a5-207">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="920a5-208">Como registrar um Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="920a5-208">How to Register a Preview Handler</span></span>](how-to-register-a-preview-handler.md)
</dt> <dt>

[<span data-ttu-id="920a5-209">Diretrizes do Gerenciador de visualização</span><span class="sxs-lookup"><span data-stu-id="920a5-209">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
