---
title: Identificador de DPI_AWARENESS_CONTEXT (windef. h)
description: Identifica o contexto de conscientização de uma janela.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295798"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="a20e3-103">Identificador de contexto de \_ reconhecimento de DPI \_</span><span class="sxs-lookup"><span data-stu-id="a20e3-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="a20e3-104">Identifica o contexto de conscientização de uma janela.</span><span class="sxs-lookup"><span data-stu-id="a20e3-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20e3-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="a20e3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a20e3-106">Constants</span></span>

<span data-ttu-id="a20e3-107">**contexto de reconhecimento de DPI sem \_ \_ \_ reconhecimento**</span><span class="sxs-lookup"><span data-stu-id="a20e3-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="a20e3-108">Sem reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-108">DPI unaware.</span></span> <span data-ttu-id="a20e3-109">Essa janela não é dimensionada para alterações de DPI e sempre é presumido ter um fator de escala de 100% (96 DPI).</span><span class="sxs-lookup"><span data-stu-id="a20e3-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="a20e3-110">Ele será dimensionado automaticamente pelo sistema em qualquer outra configuração de DPI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="a20e3-111">**\_reconhecimento do \_ sistema de contexto de reconhecimento de DPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a20e3-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="a20e3-112">Reconhecimento de DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="a20e3-112">System DPI aware.</span></span> <span data-ttu-id="a20e3-113">Essa janela não é dimensionada para alterações de DPI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="a20e3-114">Ele consultará o DPI uma vez e usará esse valor durante o tempo de vida do processo.</span><span class="sxs-lookup"><span data-stu-id="a20e3-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="a20e3-115">Se o DPI for alterado, o processo não será ajustado para o novo valor de DPI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="a20e3-116">Ele será dimensionado ou reduzido automaticamente pelo sistema quando o DPI for alterado do valor do sistema.</span><span class="sxs-lookup"><span data-stu-id="a20e3-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="a20e3-117">**contexto de reconhecimento de DPI \_ \_ \_ por \_ reconhecimento de monitor \_**</span><span class="sxs-lookup"><span data-stu-id="a20e3-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="a20e3-118">Reconhecimento de DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="a20e3-118">Per monitor DPI aware.</span></span> <span data-ttu-id="a20e3-119">Essa janela verifica o DPI quando ele é criado e ajusta o fator de escala sempre que o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="a20e3-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="a20e3-120">Esses processos não são dimensionados automaticamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="a20e3-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="a20e3-121">**Contexto de reconhecimento de DPI \_ \_ \_ por \_ reconhecimento de monitor \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="a20e3-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="a20e3-122">Também conhecido como **por monitor v2**.</span><span class="sxs-lookup"><span data-stu-id="a20e3-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="a20e3-123">Um avanço sobre o modo de reconhecimento de DPI original por monitor, que permite que os aplicativos acessem novos comportamentos de dimensionamento relacionados a DPI de acordo com cada janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="a20e3-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="a20e3-124">Por monitor v2 foi disponibilizado na atualização de criadores do Windows 10 e não está disponível em versões anteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a20e3-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="a20e3-125">Os comportamentos adicionais introduzidos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="a20e3-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="a20e3-126">**Notificações de alteração de dpi de janela filho** – em contextos de monitor v2, toda a árvore de janela é notificada sobre qualquer alteração de dpi que ocorrer.</span><span class="sxs-lookup"><span data-stu-id="a20e3-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="a20e3-127">**Dimensionamento de área de não-cliente** – todas as janelas terão automaticamente sua área que não seja de cliente desenhada de maneira sensível a dpi.</span><span class="sxs-lookup"><span data-stu-id="a20e3-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="a20e3-128">Chamadas para [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) são desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="a20e3-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="a20e3-129">**Dimensionamento de menus do Win32** – todos os menus do Ntuser criados nos contextos de acordo com o monitor v2 serão dimensionados de acordo com o monitor.</span><span class="sxs-lookup"><span data-stu-id="a20e3-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="a20e3-130">**Dimensionamento de caixa de diálogo** -caixas de diálogo do Win32 criadas nos contextos de por monitor v2 responderão automaticamente às alterações de DPI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="a20e3-131">**Dimensionamento aprimorado de controles comctl32** – vários controles comctl32 melhoraram o comportamento de dimensionamento de DPI nos contextos v2 do monitor.</span><span class="sxs-lookup"><span data-stu-id="a20e3-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="a20e3-132">**Comportamento aprimorado-os** identificadores de Uxtheme abertos no contexto de uma janela por monitor v2 funcionarão em termos do dpi associado a essa janela.</span><span class="sxs-lookup"><span data-stu-id="a20e3-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="a20e3-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="a20e3-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="a20e3-134">DPI sem reconhecimento com qualidade aprimorada de conteúdo baseado em GDI.</span><span class="sxs-lookup"><span data-stu-id="a20e3-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="a20e3-135">Esse modo se comporta de forma semelhante à DPI_AWARENESS_CONTEXT_UNAWARE, mas também permite que o sistema aprimore automaticamente a qualidade de renderização do texto e outros primitivos baseados em GDI quando a janela é exibida em um monitor de DPI alto.</span><span class="sxs-lookup"><span data-stu-id="a20e3-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="a20e3-136">Para obter mais detalhes, consulte [aprimorando a experiência de alto DPI em aplicativos de área de trabalho baseados em GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="a20e3-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="a20e3-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED foi introduzido na atualização de outubro de 2018 do Windows 10 (também conhecido como versão 1809).</span><span class="sxs-lookup"><span data-stu-id="a20e3-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="a20e3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a20e3-138">Requirements</span></span>

| <span data-ttu-id="a20e3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a20e3-139">Requirement</span></span> | <span data-ttu-id="a20e3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="a20e3-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="a20e3-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a20e3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a20e3-142">\[Somente aplicativos da área de trabalho do Windows 10, versão 1607\]</span><span class="sxs-lookup"><span data-stu-id="a20e3-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a20e3-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a20e3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a20e3-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a20e3-144">None supported</span></span> <br/>  |
| <span data-ttu-id="a20e3-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a20e3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a20e3-146"><dt>windef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a20e3-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="a20e3-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20e3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20e3-148">**AreDpiAwarenessContextsEqual**</span><span class="sxs-lookup"><span data-stu-id="a20e3-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="a20e3-149">**GetAwarenessFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-150">**GetDpiFromDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-151">**GetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-152">**GetWindowDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-153">**IsValidDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-154">**SetProcessDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="a20e3-155">**SetThreadDpiAwarenessContext**</span><span class="sxs-lookup"><span data-stu-id="a20e3-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
