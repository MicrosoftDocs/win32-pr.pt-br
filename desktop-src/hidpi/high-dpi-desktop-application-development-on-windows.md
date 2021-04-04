---
title: Desenvolvimento de aplicativos de desktop de alto DPI no Windows
description: Esse conteúdo é destinado a desenvolvedores que procuram atualizar aplicativos de área de trabalho para lidar com o fator de escala de exibição dinâmica (também conhecido como
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104084966"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a><span data-ttu-id="e39ef-103">Desenvolvimento de aplicativos de desktop de alto DPI no Windows</span><span class="sxs-lookup"><span data-stu-id="e39ef-103">High DPI Desktop Application Development on Windows</span></span>

<span data-ttu-id="e39ef-104">Esse conteúdo é destinado a desenvolvedores que procuram atualizar aplicativos de área de trabalho para lidar dinamicamente com as alterações de fator de escala de exibição (pontos por polegada ou DPI), permitindo que seus aplicativos sejam nítidos em qualquer exibição na qual são renderizados.</span><span class="sxs-lookup"><span data-stu-id="e39ef-104">This content is targeted at developers who are looking to update desktop applications to handle display scale factor (dots per inch, or DPI) changes dynamically, allowing their applications to be crisp on any display they're rendered on.</span></span>

<span data-ttu-id="e39ef-105">Para começar, se você estiver criando um novo aplicativo do Windows do zero, é altamente recomendável que você crie um aplicativo [plataforma universal do Windows (UWP)](/windows/uwp/get-started/whats-a-uwp) .</span><span class="sxs-lookup"><span data-stu-id="e39ef-105">To start, if you're creating a new Windows app from scratch, it is highly recommended that you create a [Universal Windows Platform (UWP)](/windows/uwp/get-started/whats-a-uwp) application.</span></span> <span data-ttu-id="e39ef-106">Os aplicativos UWP &mdash; &mdash; são dimensionados de forma automática e dinâmica para cada exibição em que estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="e39ef-106">UWP applications automatically&mdash;and dynamically&mdash;scale for each display that they're running on.</span></span>

<span data-ttu-id="e39ef-107">Os aplicativos de desktop que usam tecnologias mais antigas de programação do Windows (programação pura do Win32, Windows Forms, Windows Presentation Framework (WPF) etc.) não conseguem lidar automaticamente com o dimensionamento de DPI sem o trabalho adicional do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="e39ef-107">Desktop applications using older Windows programming technologies (raw Win32 programming, Windows Forms, Windows Presentation Framework (WPF), etc.) are unable to automatically handle DPI scaling without additional developer work.</span></span> <span data-ttu-id="e39ef-108">Sem tal trabalho, os aplicativos aparecerão borrados ou incorretamente dimensionados em muitos cenários de uso comuns.</span><span class="sxs-lookup"><span data-stu-id="e39ef-108">Without such work, applications will appear blurry or incorrectly-sized in many common usage scenarios.</span></span> <span data-ttu-id="e39ef-109">Este documento fornece contexto e informações sobre o que está envolvido na atualização de um aplicativo de área de trabalho para renderização correta.</span><span class="sxs-lookup"><span data-stu-id="e39ef-109">This document provides context and information about what is involved in updating a desktop application to render correctly.</span></span>

## <a name="display-scale-factor--dpi"></a><span data-ttu-id="e39ef-110">Exibir fator de escala & DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-110">Display Scale Factor & DPI</span></span>

<span data-ttu-id="e39ef-111">À medida que a tecnologia de vídeo progrediu, os fabricantes de painel de exibição lançaram um número cada vez maior de pixels em cada unidade de espaço físico em seus painéis.</span><span class="sxs-lookup"><span data-stu-id="e39ef-111">As display technology has progressed, display panel manufacturers have packed an increasing number of pixels into each unit of physical space on their panels.</span></span> <span data-ttu-id="e39ef-112">Isso resultou em pontos por polegada (DPI) dos painéis de exibição modernos sendo muito maiores do que historicamente.</span><span class="sxs-lookup"><span data-stu-id="e39ef-112">This has resulted in the dots per inch (DPI) of modern display panels being much higher than they have historically been.</span></span> <span data-ttu-id="e39ef-113">No passado, a maioria dos monitores tinha 96 pixels por polegada linear de espaço físico (96 DPI); no 2017, os monitores com quase 300 DPI ou mais estão prontamente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e39ef-113">In the past, most displays had 96 pixels per linear inch of physical space (96 DPI); in 2017, displays with nearly 300 DPI or higher are readily available.</span></span>

<span data-ttu-id="e39ef-114">A maioria das estruturas de interface do usuário da área de trabalho herdada tem suposições internas de que o DPI de vídeo não será alterado durante o tempo de vida do processo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-114">Most legacy desktop UI frameworks have built-in assumptions that the display DPI will not change during the lifetime of the process.</span></span>  <span data-ttu-id="e39ef-115">Essa suposição não é mais verdadeira, com o DPIs de exibição geralmente mudando várias vezes durante o tempo de vida de um processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-115">This assumption no longer holds true, with display DPIs commonly changing several times throughout an application process's lifetime.</span></span> <span data-ttu-id="e39ef-116">Alguns cenários comuns em que as alterações de fator de escala de exibição/DPI são:</span><span class="sxs-lookup"><span data-stu-id="e39ef-116">Some common scenarios where the display scale factor/DPI changes are:</span></span>

-   <span data-ttu-id="e39ef-117">Configurações de monitores múltiplos em que cada exibição tem um fator de escala diferente e o aplicativo é movido de uma exibição para outra (como uma exibição de 4K e 1080p)</span><span class="sxs-lookup"><span data-stu-id="e39ef-117">Multiple-monitor setups where each display has a different scale factor and the application is moved from one display to another (such as a 4K and a 1080p display)</span></span>
-   <span data-ttu-id="e39ef-118">Encaixe e desencaixe de um laptop de DPI alto com uma exibição externa de DPI baixo (ou vice-versa)</span><span class="sxs-lookup"><span data-stu-id="e39ef-118">Docking and undocking a high DPI laptop with a low-DPI external display (or vice versa)</span></span>
-   <span data-ttu-id="e39ef-119">Conectar-se via Área de Trabalho Remota de um laptop/Tablet de DPI alto a um dispositivo de baixo DPI (ou vice-versa)</span><span class="sxs-lookup"><span data-stu-id="e39ef-119">Connecting via Remote Desktop from a high DPI laptop/tablet to a low-DPI device (or vice versa)</span></span>
-   <span data-ttu-id="e39ef-120">Alterando as configurações do fator de escala de exibição enquanto os aplicativos estão em execução</span><span class="sxs-lookup"><span data-stu-id="e39ef-120">Making a display-scale-factor settings change while applications are running</span></span>

<span data-ttu-id="e39ef-121">Nesses cenários, os aplicativos UWP redesenham-se para o novo DPI automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e39ef-121">In these scenarios, UWP applications redraw themselves for the new DPI automatically.</span></span> <span data-ttu-id="e39ef-122">Por padrão, e sem trabalho adicional para desenvolvedores, os aplicativos de área de trabalho não.</span><span class="sxs-lookup"><span data-stu-id="e39ef-122">By default, and without additional developer work, desktop applications do not.</span></span> <span data-ttu-id="e39ef-123">Os aplicativos de área de trabalho que não fazem esse trabalho extra para responder às alterações de DPI podem aparecer borrados ou ter um tamanho incorreto para o usuário.</span><span class="sxs-lookup"><span data-stu-id="e39ef-123">Desktop applications that don't do this extra work to respond to DPI changes may appear blurry or incorrectly-sized to the user.</span></span>

## <a name="dpi-awareness-mode"></a><span data-ttu-id="e39ef-124">Modo de reconhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-124">DPI Awareness Mode</span></span>

<span data-ttu-id="e39ef-125">Os aplicativos da área de trabalho devem informar ao Windows se eles dão suporte ao dimensionamento de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-125">Desktop applications must tell Windows if they support DPI scaling.</span></span> <span data-ttu-id="e39ef-126">Por padrão, o sistema considera o DPI dos aplicativos de desktop sem reconhecimento e bitmap – amplia suas janelas.</span><span class="sxs-lookup"><span data-stu-id="e39ef-126">By default, the system considers desktop applications DPI unaware and bitmap-stretches their windows.</span></span> <span data-ttu-id="e39ef-127">Ao definir um dos seguintes modos de reconhecimento de DPI disponíveis, os aplicativos podem dizer explicitamente ao Windows como eles desejam lidar com o dimensionamento de DPI:</span><span class="sxs-lookup"><span data-stu-id="e39ef-127">By setting one of the following available DPI awareness modes, applications can explicitly tell Windows how they wish to handle DPI scaling:</span></span>

### <a name="dpi-unaware"></a><span data-ttu-id="e39ef-128">Sem reconhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-128">DPI Unaware</span></span>

<span data-ttu-id="e39ef-129">Aplicativos sem reconhecimento de DPI renderizam em um valor de DPI fixo de 96 (100%).</span><span class="sxs-lookup"><span data-stu-id="e39ef-129">DPI unaware applications render at a fixed DPI value of 96 (100%).</span></span> <span data-ttu-id="e39ef-130">Sempre que esses aplicativos são executados em uma tela com uma escala de exibição maior que 96 DPI, o Windows vai alongar o bitmap do aplicativo para o tamanho físico esperado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-130">Whenever these applications are run on a screen with a display scale greater than 96 DPI, Windows will stretch the application bitmap to the expected physical size.</span></span> <span data-ttu-id="e39ef-131">Isso resulta na exibição desfoque do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-131">This results in the application appearing blurry.</span></span>

### <a name="system-dpi-awareness"></a><span data-ttu-id="e39ef-132">Reconhecimento de DPI do sistema</span><span class="sxs-lookup"><span data-stu-id="e39ef-132">System DPI Awareness</span></span>

<span data-ttu-id="e39ef-133">Os aplicativos de desktop com reconhecimento de DPI do sistema normalmente recebem o DPI do monitor conectado primário a partir do momento da entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="e39ef-133">Desktop applications that are system DPI aware typically receive the DPI of the primary connected monitor as of the time of user sign-in.</span></span> <span data-ttu-id="e39ef-134">Durante a inicialização, eles formam sua interface do usuário adequadamente (controles de dimensionamento, escolhendo tamanhos de fonte, carregando ativos, etc.) usando esse valor de DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="e39ef-134">During initialization, they lay out their UI appropriately (sizing controls, choosing font sizes, loading assets, etc.) using that System DPI value.</span></span> <span data-ttu-id="e39ef-135">Assim, os aplicativos com reconhecimento de DPI do sistema não são escalares de DPI (bitmap ampliado) pelo Windows no exibe a renderização naquele único DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-135">As such, System DPI-aware applications are not DPI scaled (bitmap stretched) by Windows on displays rendering at that single DPI.</span></span> <span data-ttu-id="e39ef-136">Quando o aplicativo é movido para uma exibição com um fator de escala diferente, ou se o fator de escala de exibição for alterado, o Windows fará o bitmap dimensionar as janelas do aplicativo, tornando-as aparentemente borradas.</span><span class="sxs-lookup"><span data-stu-id="e39ef-136">When the application is moved to a display with a different scale factor, or if the display scale factor otherwise changes, Windows will bitmap scale the application's windows, making them appear blurry.</span></span> <span data-ttu-id="e39ef-137">Efetivamente, os aplicativos de área de trabalho com reconhecimento de DPI do sistema são processados de forma nítida em um único fator de escala de exibição, ficando desfocado sempre que o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-137">Effectively, System DPI-aware desktop applications only render crisply at a single display scale factor, becoming blurry whenever the DPI changes.</span></span>

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a><span data-ttu-id="e39ef-138">Reconhecimento de DPI de Per-Monitor e Per-Monitor (v2)</span><span class="sxs-lookup"><span data-stu-id="e39ef-138">Per-Monitor and Per-Monitor (V2) DPI Awareness</span></span>

<span data-ttu-id="e39ef-139">É recomendável que os aplicativos da área de trabalho sejam atualizados para usar o modo de reconhecimento de DPI por monitor, permitindo que eles sejam renderizados imediatamente sempre que o DPI for alterado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-139">It is recommended that desktop applications be updated to use per-monitor DPI awareness mode, allowing them to immediately render correctly whenever the DPI changes.</span></span> <span data-ttu-id="e39ef-140">Quando um aplicativo se reporta ao Windows que deseja executar nesse modo, o Windows não bitmap amplia o aplicativo quando o DPI muda, em vez disso, envia o [WM \_ DPICHANGED](wm-dpichanged.md) para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-140">When an application reports to Windows that it wants to run in this mode, Windows will not bitmap stretch the application when the DPI changes, instead sending [WM\_DPICHANGED](wm-dpichanged.md) to the application window.</span></span> <span data-ttu-id="e39ef-141">Em seguida, é responsabilidade total do aplicativo lidar com o redimensionamento para o novo DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-141">It is then the complete responsibility of the application to handle resizing itself for the new DPI.</span></span> <span data-ttu-id="e39ef-142">A maioria das estruturas de interface do usuário usadas por aplicativos de desktop (comctl32), Windows Forms, Windows Presentation Framework, etc.) não dão suporte ao dimensionamento automático de DPI, exigindo que os desenvolvedores redimensionem e reposicionem o conteúdo de suas próprias janelas.</span><span class="sxs-lookup"><span data-stu-id="e39ef-142">Most UI frameworks used by desktop applications (Windows common controls (comctl32), Windows Forms, Windows Presentation Framework, etc.) do not support automatic DPI scaling, requiring developers to resize and reposition the contents of their windows themselves.</span></span>

<span data-ttu-id="e39ef-143">Há duas versões do Per-Monitor reconhecimento de que um aplicativo pode se registrar como: versão 1 e versão 2 (PMv2).</span><span class="sxs-lookup"><span data-stu-id="e39ef-143">There are two versions of Per-Monitor awareness that an application can register itself as: version 1 and version 2 (PMv2).</span></span> <span data-ttu-id="e39ef-144">O registro de um processo como executado no modo de reconhecimento de PMv2 resulta em:</span><span class="sxs-lookup"><span data-stu-id="e39ef-144">Registering a process as running in PMv2 awareness mode results in:</span></span>

1.  <span data-ttu-id="e39ef-145">O aplicativo que está sendo notificado quando o DPI é alterado (ambos os HWNDs de nível superior e filho)</span><span class="sxs-lookup"><span data-stu-id="e39ef-145">The application being notified when the DPI changes (both the top-level and child HWNDs)</span></span>
2.  <span data-ttu-id="e39ef-146">O aplicativo que vê os pixels brutos de cada exibição</span><span class="sxs-lookup"><span data-stu-id="e39ef-146">The application seeing the raw pixels of each display</span></span>
3.  <span data-ttu-id="e39ef-147">O aplicativo nunca é um bitmap dimensionado pelo Windows</span><span class="sxs-lookup"><span data-stu-id="e39ef-147">The application never being bitmap scaled by Windows</span></span>
4.  <span data-ttu-id="e39ef-148">Área não cliente automática (legenda da janela, barras de rolagem, etc.) Escala de DPI pelo Windows</span><span class="sxs-lookup"><span data-stu-id="e39ef-148">Automatic non-client area (window caption, scroll bars, etc.) DPI scaling by Windows</span></span>
5.  <span data-ttu-id="e39ef-149">Caixas de diálogo do Win32 (de [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automaticamente dpi dimensionada pelo Windows</span><span class="sxs-lookup"><span data-stu-id="e39ef-149">Win32 dialogs (from [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatically DPI scaled by Windows</span></span>
6.  <span data-ttu-id="e39ef-150">Os ativos de bitmap desenhado por tema em controles comuns (caixas de seleção, planos de fundo de botão, etc.) são automaticamente renderizados no fator de escala de DPI apropriado</span><span class="sxs-lookup"><span data-stu-id="e39ef-150">Theme-drawn bitmap assets in common controls (checkboxes, button backgrounds, etc.) being automatically rendered at the appropriate DPI scale factor</span></span>

<span data-ttu-id="e39ef-151">Ao executar no modo de reconhecimento de Per-Monitor v2, os aplicativos são notificados quando seu DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-151">When running in Per-Monitor v2 Awareness mode, applications are notified when their DPI has changed.</span></span> <span data-ttu-id="e39ef-152">Se um aplicativo não se redimensionar para o novo DPI, a interface do usuário do aplicativo aparecerá muito pequena ou muito grande (dependendo da diferença nos valores de DPI anterior e novo).</span><span class="sxs-lookup"><span data-stu-id="e39ef-152">If an application does not resize itself for the new DPI, the application UI will appear too small or too large (depending on the difference in the previous and new DPI values).</span></span>

> [!Note]  
> <span data-ttu-id="e39ef-153">A conscientização do Per-Monitor V1 (PMv1) é muito limitada.</span><span class="sxs-lookup"><span data-stu-id="e39ef-153">Per-Monitor V1 (PMv1) awareness is very limited.</span></span> <span data-ttu-id="e39ef-154">É recomendável que os aplicativos usem o PMv2.</span><span class="sxs-lookup"><span data-stu-id="e39ef-154">It is recommended that applications use PMv2.</span></span>

<span data-ttu-id="e39ef-155">A tabela a seguir mostra como os aplicativos serão renderizados em diferentes cenários:</span><span class="sxs-lookup"><span data-stu-id="e39ef-155">The following table shows how applications will render under different scenarios:</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e39ef-156">Modo de reconhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-156">DPI Awareness Mode</span></span></th>
<th><span data-ttu-id="e39ef-157">Versão do Windows introduzida</span><span class="sxs-lookup"><span data-stu-id="e39ef-157">Windows Version Introduced</span></span></th>
<th><span data-ttu-id="e39ef-158">Modo de exibição do aplicativo de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-158">Application's view of DPI</span></span></th>
<th><span data-ttu-id="e39ef-159">Comportamento na alteração de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-159">Behavior on DPI change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e39ef-160">Conhecida</span><span class="sxs-lookup"><span data-stu-id="e39ef-160">Unaware</span></span></td>
<td><span data-ttu-id="e39ef-161">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-161">N/A</span></span></td>
<td><span data-ttu-id="e39ef-162">Todas as telas são 96 DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-162">All displays are 96 DPI</span></span></td>
<td><span data-ttu-id="e39ef-163">Alongamento de bitmap (borrado)</span><span class="sxs-lookup"><span data-stu-id="e39ef-163">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e39ef-164">Sistema</span><span class="sxs-lookup"><span data-stu-id="e39ef-164">System</span></span></td>
<td><span data-ttu-id="e39ef-165">Vista</span><span class="sxs-lookup"><span data-stu-id="e39ef-165">Vista</span></span></td>
<td><span data-ttu-id="e39ef-166">Todos os monitores têm o mesmo DPI (o DPI da exibição primária no momento em que a sessão do usuário atual foi iniciada)</span><span class="sxs-lookup"><span data-stu-id="e39ef-166">All displays have the same DPI (the DPI of the primary display at the time the current user session was started)</span></span></td>
<td><span data-ttu-id="e39ef-167">Alongamento de bitmap (borrado)</span><span class="sxs-lookup"><span data-stu-id="e39ef-167">Bitmap-stretching (blurry)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e39ef-168">Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="e39ef-168">Per-Monitor</span></span></td>
<td><span data-ttu-id="e39ef-169">8.1</span><span class="sxs-lookup"><span data-stu-id="e39ef-169">8.1</span></span></td>
<td><span data-ttu-id="e39ef-170">O DPI da exibição na qual a janela do aplicativo está localizada principalmente</span><span class="sxs-lookup"><span data-stu-id="e39ef-170">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="e39ef-171">O HWND de nível superior é notificado de alteração de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-171">Top-level HWND is notified of DPI change</span></span></li>
<li><span data-ttu-id="e39ef-172">Sem ajuste de DPI de nenhum elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e39ef-172">No DPI scaling of any UI elements.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e39ef-173">Per-Monitor V2</span><span class="sxs-lookup"><span data-stu-id="e39ef-173">Per-Monitor V2</span></span></td>
<td><span data-ttu-id="e39ef-174">Atualização do Windows 10 para criadores (1703)</span><span class="sxs-lookup"><span data-stu-id="e39ef-174">Windows 10 Creators Update (1703)</span></span></td>
<td><span data-ttu-id="e39ef-175">O DPI da exibição na qual a janela do aplicativo está localizada principalmente</span><span class="sxs-lookup"><span data-stu-id="e39ef-175">The DPI of the display that the application window is primarily located on</span></span></td>
<td><ul>
<li><span data-ttu-id="e39ef-176">Os HWNDs de nível superior <span class="underline">e</span> filho são notificados da alteração de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-176">Top-level <span class="underline">and</span> child HWNDs are notified of DPI change</span></span></li>
</ul>
<br/> <span data-ttu-id="e39ef-177"><span class="underline">Ajuste automático de DPI de:</span>
</span><span class="sxs-lookup"><span data-stu-id="e39ef-177"><span class="underline">Automatic DPI scaling of:</span>
</span></span><ul>
<li><span data-ttu-id="e39ef-178">Área não cliente</span><span class="sxs-lookup"><span data-stu-id="e39ef-178">Non-client area</span></span></li>
<li><span data-ttu-id="e39ef-179">Bitmaps desenhados por tema em controles comuns (comctl32 V6)</span><span class="sxs-lookup"><span data-stu-id="e39ef-179">Theme-drawn bitmaps in common controls (comctl32 V6)</span></span></li>
<li><span data-ttu-id="e39ef-180">Caixas de diálogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span><span class="sxs-lookup"><span data-stu-id="e39ef-180">Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a><span data-ttu-id="e39ef-181">Reconhecimento de DPI por monitor (v1)</span><span class="sxs-lookup"><span data-stu-id="e39ef-181">Per Monitor (V1) DPI Awareness</span></span>

<span data-ttu-id="e39ef-182">O modo de reconhecimento de Per-Monitor v1 DPI (PMv1) foi introduzido com Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="e39ef-182">Per-Monitor V1 DPI awareness mode (PMv1) was introduced with Windows 8.1.</span></span> <span data-ttu-id="e39ef-183">Esse modo de reconhecimento de DPI é muito limitado e oferece apenas a funcionalidade listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-183">This DPI awareness mode is very limited and only offers the functionality listed below.</span></span> <span data-ttu-id="e39ef-184">É recomendável que os aplicativos de desktop usem o modo de reconhecimento v2 Per-Monitor, com suporte no Windows 10 1703 ou superior.</span><span class="sxs-lookup"><span data-stu-id="e39ef-184">It is recommended that desktop applications use Per-Monitor v2 awareness mode, supported on Windows 10 1703 or above.</span></span>

<span data-ttu-id="e39ef-185">O suporte inicial para reconhecimento por monitor oferecia apenas os aplicativos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e39ef-185">The initial support for per-monitor awareness only offered applications the following:</span></span>

1.  <span data-ttu-id="e39ef-186">Os HWNDs de nível superior são notificados de uma alteração de DPI e fornecem um novo tamanho sugerido</span><span class="sxs-lookup"><span data-stu-id="e39ef-186">Top-level HWNDs are notified of a DPI change and provided a new suggested size</span></span>
2.  <span data-ttu-id="e39ef-187">O Windows não ampliará o bitmap da interface do usuário do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e39ef-187">Windows will not bitmap stretch the application UI</span></span>
3.  <span data-ttu-id="e39ef-188">O aplicativo vê todas as telas em pixels físicos (consulte virtualização)</span><span class="sxs-lookup"><span data-stu-id="e39ef-188">The application sees all displays in physical pixels (see virtualization)</span></span>

<span data-ttu-id="e39ef-189">No Windows 10 1607 ou superior, os aplicativos PMv1 também podem chamar [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante \_ o WM NCCREATE para solicitar que o Windows dimensione corretamente a área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="e39ef-189">On Windows 10 1607 or above, PMv1 applications may also call [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) during WM\_NCCREATE to request that Windows correctly scale the window's non-client area.</span></span>

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a><span data-ttu-id="e39ef-190">Suporte ao dimensionamento de DPI por monitor pela estrutura/tecnologia da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e39ef-190">Per Monitor DPI Scaling Support by UI Framework / Technology</span></span>

<span data-ttu-id="e39ef-191">A tabela a seguir mostra o nível de suporte de reconhecimento de DPI por monitor oferecido por várias estruturas da interface do usuário do Windows a partir do Windows 10 1703:</span><span class="sxs-lookup"><span data-stu-id="e39ef-191">The table below shows the level of per-monitor DPI awareness support offered by various Windows UI frameworks as of Windows 10 1703:</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e39ef-192">Estrutura/tecnologia</span><span class="sxs-lookup"><span data-stu-id="e39ef-192">Framework / Technology</span></span></th>
<th><span data-ttu-id="e39ef-193">Suporte</span><span class="sxs-lookup"><span data-stu-id="e39ef-193">Support</span></span></th>
<th><span data-ttu-id="e39ef-194">Versão do SO</span><span class="sxs-lookup"><span data-stu-id="e39ef-194">OS Version</span></span></th>
<th><span data-ttu-id="e39ef-195">Escala de DPI manipulada por</span><span class="sxs-lookup"><span data-stu-id="e39ef-195">DPI Scaling handled by</span></span></th>
<th><span data-ttu-id="e39ef-196">Leitura Adicional</span><span class="sxs-lookup"><span data-stu-id="e39ef-196">Further Reading</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e39ef-197">Plataforma Universal do Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="e39ef-197">Universal Windows Platform (UWP)</span></span></td>
<td><span data-ttu-id="e39ef-198">Completo</span><span class="sxs-lookup"><span data-stu-id="e39ef-198">Full</span></span></td>
<td><span data-ttu-id="e39ef-199">1607</span><span class="sxs-lookup"><span data-stu-id="e39ef-199">1607</span></span></td>
<td><span data-ttu-id="e39ef-200">Estrutura de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e39ef-200">UI framework</span></span></td>
<td><span data-ttu-id="e39ef-201"><a href="/windows/uwp/get-started/whats-a-uwp">UWP (Plataforma Universal do Windows)</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-201"><a href="/windows/uwp/get-started/whats-a-uwp">Universal Windows Platform (UWP)</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e39ef-202">Controles Win32/comuns V6 brutos (comctl32.dll)</span><span class="sxs-lookup"><span data-stu-id="e39ef-202">Raw Win32/Common Controls V6 (comctl32.dll)</span></span></td>
<td><ul>
<li><span data-ttu-id="e39ef-203">Mensagens de notificação de alteração de DPI enviadas a todos os HWNDs</span><span class="sxs-lookup"><span data-stu-id="e39ef-203">DPI change notification messages sent to all HWNDs</span></span></li>
<li><span data-ttu-id="e39ef-204">Os ativos de tema desenhado são renderizados corretamente em controles comuns</span><span class="sxs-lookup"><span data-stu-id="e39ef-204">Theme-drawn assets render correctly in common controls</span></span></li>
<li><span data-ttu-id="e39ef-205">Dimensionamento automático de DPI para caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="e39ef-205">Automatic DPI scaling for dialogs</span></span></li>
</ul></td>
<td><span data-ttu-id="e39ef-206">1703</span><span class="sxs-lookup"><span data-stu-id="e39ef-206">1703</span></span></td>
<td><span data-ttu-id="e39ef-207">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e39ef-207">Application</span></span></td>
<td><span data-ttu-id="e39ef-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Exemplo do GitHub</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-208"><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e39ef-209">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e39ef-209">Windows Forms</span></span></td>
<td><span data-ttu-id="e39ef-210">Dimensionamento automático limitado por monitor de DPI para alguns controles</span><span class="sxs-lookup"><span data-stu-id="e39ef-210">Limited automatic per-monitor DPI scaling for some controls</span></span></td>
<td><span data-ttu-id="e39ef-211">1703</span><span class="sxs-lookup"><span data-stu-id="e39ef-211">1703</span></span></td>
<td><span data-ttu-id="e39ef-212">Estrutura de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e39ef-212">UI framework</span></span></td>
<td><span data-ttu-id="e39ef-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Suporte a alto DPI no Windows Forms</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-213"><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">High DPI Support in Windows Forms</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e39ef-214">Windows Presentation Framework (WPF)</span><span class="sxs-lookup"><span data-stu-id="e39ef-214">Windows Presentation Framework (WPF)</span></span></td>
<td><span data-ttu-id="e39ef-215">Os aplicativos nativos do WPF terão a escala de DPI do WPF hospedado em outras estruturas e outras estruturas hospedadas no WPF não são dimensionadas automaticamente</span><span class="sxs-lookup"><span data-stu-id="e39ef-215">Native WPF applications will DPI scale WPF hosted in other frameworks and other frameworks hosted in WPF do not automatically scale</span></span></td>
<td><span data-ttu-id="e39ef-216">1607</span><span class="sxs-lookup"><span data-stu-id="e39ef-216">1607</span></span></td>
<td><span data-ttu-id="e39ef-217">Estrutura de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="e39ef-217">UI framework</span></span></td>
<td><span data-ttu-id="e39ef-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Exemplo do GitHub</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-218"><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Sample</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e39ef-219">GDI</span><span class="sxs-lookup"><span data-stu-id="e39ef-219">GDI</span></span></td>
<td><span data-ttu-id="e39ef-220">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e39ef-220">None</span></span></td>
<td><span data-ttu-id="e39ef-221">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-221">N/A</span></span></td>
<td><span data-ttu-id="e39ef-222">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e39ef-222">Application</span></span></td>
<td><span data-ttu-id="e39ef-223">Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-223">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e39ef-224">GDI+</span><span class="sxs-lookup"><span data-stu-id="e39ef-224">GDI+</span></span></td>
<td><span data-ttu-id="e39ef-225">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e39ef-225">None</span></span></td>
<td><span data-ttu-id="e39ef-226">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-226">N/A</span></span></td>
<td><span data-ttu-id="e39ef-227">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e39ef-227">Application</span></span></td>
<td><span data-ttu-id="e39ef-228">Consulte <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">dimensionamento de dpi alta do GDI</a></span><span class="sxs-lookup"><span data-stu-id="e39ef-228">See <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e39ef-229">MFC</span><span class="sxs-lookup"><span data-stu-id="e39ef-229">MFC</span></span></td>
<td><span data-ttu-id="e39ef-230">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e39ef-230">None</span></span></td>
<td><span data-ttu-id="e39ef-231">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-231">N/A</span></span></td>
<td><span data-ttu-id="e39ef-232">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e39ef-232">Application</span></span></td>
<td><span data-ttu-id="e39ef-233">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-233">N/A</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a><span data-ttu-id="e39ef-234">Atualizando aplicativos existentes</span><span class="sxs-lookup"><span data-stu-id="e39ef-234">Updating Existing Applications</span></span>

<span data-ttu-id="e39ef-235">Para atualizar um aplicativo de área de trabalho existente para manipular o dimensionamento de DPI corretamente, ele precisa ser atualizado de modo que, no mínimo, as partes importantes de sua interface do usuário sejam atualizadas para responder a alterações de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-235">In order to update an existing desktop application to handle DPI scaling properly, it needs to be updated such that, at a minimum, the important parts of its UI are updated to respond to DPI changes.</span></span>

<span data-ttu-id="e39ef-236">A maioria dos aplicativos de desktop é executada no modo de reconhecimento de DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="e39ef-236">Most desktop applications run under system DPI awareness mode.</span></span> <span data-ttu-id="e39ef-237">Aplicativos com reconhecimento de DPI de sistema normalmente são dimensionados para o DPI da exibição primária (a exibição na qual a bandeja do sistema estava localizada no momento em que a sessão do Windows foi iniciada).</span><span class="sxs-lookup"><span data-stu-id="e39ef-237">System-DPI-aware applications typically scale to the DPI of the primary display (the display that the system tray was located on at the time the Windows session was started).</span></span> <span data-ttu-id="e39ef-238">Quando o DPI é alterado, o Windows bitmap amplia a interface do usuário desses aplicativos, o que geralmente resulta na desfoque.</span><span class="sxs-lookup"><span data-stu-id="e39ef-238">When the DPI changes, Windows will bitmap stretch the UI of these applications, which often results in them being blurry.</span></span> <span data-ttu-id="e39ef-239">Ao atualizar um aplicativo com reconhecimento de DPI do sistema para se tornar ciente por monitor-DPI, o código que manipula o layout da interface do usuário precisa ser atualizado, de modo que ele seja executado não apenas durante a inicialização do aplicativo, mas também sempre que uma notificação de alteração de DPI ([WM \_ DPICHANGED](wm-dpichanged.md) no caso do Win32) for recebida.</span><span class="sxs-lookup"><span data-stu-id="e39ef-239">When updating a System DPI-aware application to become per-monitor-DPI aware, the code which handles UI layout needs to be updated such that it is performed not only during application initialization, but also whenever a DPI change notification ([WM\_DPICHANGED](wm-dpichanged.md) in the case of Win32) is received.</span></span> <span data-ttu-id="e39ef-240">Isso geralmente envolve a revisita de qualquer suposição no código que a interface do usuário só precisa ser dimensionada uma vez.</span><span class="sxs-lookup"><span data-stu-id="e39ef-240">This typically involves revisiting any assumptions in the code that the UI only needs to be scaled once.</span></span>

<span data-ttu-id="e39ef-241">Além disso, no caso da programação Win32, muitas APIs do Win32 não têm nenhum contexto de vídeo ou DPI para que eles retornem apenas valores relativos ao DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="e39ef-241">Also, in the case of Win32 programming, many Win32 APIs do not have any DPI or display context so they will only return values relative to the System DPI.</span></span> <span data-ttu-id="e39ef-242">Pode ser útil fazer o grep por meio de seu código para procurar algumas dessas APIs e substituí-las por variantes com reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-242">It can be useful to grep through your code to look for some of these APIs and replace them with DPI-aware variants.</span></span> <span data-ttu-id="e39ef-243">Algumas das APIs comuns que têm variantes com reconhecimento de DPI são:</span><span class="sxs-lookup"><span data-stu-id="e39ef-243">Some of the common APIs that have DPI-aware variants are:</span></span>



| <span data-ttu-id="e39ef-244">Versão de DPI única</span><span class="sxs-lookup"><span data-stu-id="e39ef-244">Single DPI version</span></span>   | <span data-ttu-id="e39ef-245">Versão do Per-Monitor</span><span class="sxs-lookup"><span data-stu-id="e39ef-245">Per-Monitor version</span></span>        |
|----------------------|----------------------------|
| <span data-ttu-id="e39ef-246">GetSystemMetrics</span><span class="sxs-lookup"><span data-stu-id="e39ef-246">GetSystemMetrics</span></span>     | <span data-ttu-id="e39ef-247">GetSystemMetricsForDpi</span><span class="sxs-lookup"><span data-stu-id="e39ef-247">GetSystemMetricsForDpi</span></span>     |
| <span data-ttu-id="e39ef-248">AdjustWindowRectEx</span><span class="sxs-lookup"><span data-stu-id="e39ef-248">AdjustWindowRectEx</span></span>   | <span data-ttu-id="e39ef-249">AdjustWindowRectExForDpi</span><span class="sxs-lookup"><span data-stu-id="e39ef-249">AdjustWindowRectExForDpi</span></span>   |
| <span data-ttu-id="e39ef-250">SystemParametersInfo</span><span class="sxs-lookup"><span data-stu-id="e39ef-250">SystemParametersInfo</span></span> | <span data-ttu-id="e39ef-251">SystemParametersInfoForDpi</span><span class="sxs-lookup"><span data-stu-id="e39ef-251">SystemParametersInfoForDpi</span></span> |
| <span data-ttu-id="e39ef-252">GetDpiForMonitor</span><span class="sxs-lookup"><span data-stu-id="e39ef-252">GetDpiForMonitor</span></span>     | <span data-ttu-id="e39ef-253">GetDpiForWindow</span><span class="sxs-lookup"><span data-stu-id="e39ef-253">GetDpiForWindow</span></span>            |



 

<span data-ttu-id="e39ef-254">Também é uma boa ideia Pesquisar os tamanhos embutidos em código na sua codebase que assumem um DPI constante, substituindo-os pelo código que conta corretamente no dimensionamento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-254">It is also a good idea to search for hard-coded sizes in your codebase that assume a constant DPI, replacing them with code that correctly accounts for DPI scaling.</span></span> <span data-ttu-id="e39ef-255">Veja abaixo um exemplo que incorpora todas essas sugestões:</span><span class="sxs-lookup"><span data-stu-id="e39ef-255">Below is an example that incorporates all of these suggestions:</span></span>

### <a name="example"></a><span data-ttu-id="e39ef-256">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="e39ef-256">Example:</span></span>

<span data-ttu-id="e39ef-257">O exemplo a seguir mostra um caso do Win32 simplificado de criar um HWND filho.</span><span class="sxs-lookup"><span data-stu-id="e39ef-257">The example below shows a simplified Win32 case of creating a child HWND.</span></span> <span data-ttu-id="e39ef-258">A chamada para CreateWindow pressupõe que o aplicativo está sendo executado às 96 DPI, e nem o tamanho do botão nem a posição estarão corretos em DPIs maiores:</span><span class="sxs-lookup"><span data-stu-id="e39ef-258">The call to CreateWindow assumes that the application is running at 96 DPI, and neither the button's size nor position will be correct at higher DPIs:</span></span>


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



<span data-ttu-id="e39ef-259">O código atualizado abaixo mostra:</span><span class="sxs-lookup"><span data-stu-id="e39ef-259">The updated code below shows:</span></span>

1.  <span data-ttu-id="e39ef-260">O DPI de código de criação de janela dimensionando a posição e o tamanho do HWND filho para o DPI de sua janela pai</span><span class="sxs-lookup"><span data-stu-id="e39ef-260">The window-creation code DPI scaling the position and size of the child HWND for the DPI of its parent window</span></span>
2.  <span data-ttu-id="e39ef-261">Respondendo à alteração de DPI reposicionando e redimensionando o HWND filho</span><span class="sxs-lookup"><span data-stu-id="e39ef-261">Responding to DPI change by repositioning and resizing the child HWND</span></span>
3.  <span data-ttu-id="e39ef-262">Tamanhos embutidos em código removidos e substituídos por código que responde a alterações de DPI</span><span class="sxs-lookup"><span data-stu-id="e39ef-262">Hard-coded sizes removed and replaced with code that responds to DPI changes</span></span>


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



<span data-ttu-id="e39ef-263">Ao atualizar um aplicativo com reconhecimento de DPI do sistema, algumas etapas comuns a serem seguidas são:</span><span class="sxs-lookup"><span data-stu-id="e39ef-263">When updating a System DPI-aware application, some common steps to follow are:</span></span>

1.  <span data-ttu-id="e39ef-264">Marque o processo como reconhecimento de DPI por monitor (v2) usando um manifesto de aplicativo (ou outro método, dependendo das estruturas de interface do usuário usadas).</span><span class="sxs-lookup"><span data-stu-id="e39ef-264">Mark the process as per-monitor DPI aware (V2) using an application manifest (or other method, depending on the UI framework(s) used).</span></span>
2.  <span data-ttu-id="e39ef-265">Torne a lógica de layout da interface do usuário reutilizável e mova-a para fora do código de inicialização do aplicativo, de modo que ela possa ser reutilizada quando ocorrer uma alteração de DPI (WM \_ DPICHANGED no caso da programação do Windows (Win32)).</span><span class="sxs-lookup"><span data-stu-id="e39ef-265">Make UI layout logic reusable and move it out of application-initialization code such that it can be reused when a DPI change occurs (WM\_DPICHANGED in the case of Windows (Win32) programming).</span></span>
3.  <span data-ttu-id="e39ef-266">Invalidar qualquer código que assuma que os dados sensíveis a DPI (DPI/fontes/tamanhos/etc.) nunca precisem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="e39ef-266">Invalidate any code that assumes that DPI-sensitive data (DPI/fonts/sizes/etc.) never need to be updated.</span></span> <span data-ttu-id="e39ef-267">É uma prática muito comum armazenar em cache os tamanhos de fonte e valores de DPI na inicialização do processo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-267">It is a very common practice to cache font sizes and DPI values at process initialization.</span></span> <span data-ttu-id="e39ef-268">Ao atualizar um aplicativo para se tornar um reconhecimento de DPI por monitor, os dados sensíveis a DPI devem ser reavaliados sempre que um novo DPI for encontrado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-268">When updating an application to become per-monitor DPI aware, DPI-sensitive data must be reevaluated whenever a new DPI is encountered.</span></span>
4.  <span data-ttu-id="e39ef-269">Quando ocorre uma alteração de DPI, recarregar (ou rerasterizar) todos os ativos de bitmap para o novo DPI ou, opcionalmente, ampliar os ativos carregados no momento para o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="e39ef-269">When a DPI change occurs, reload (or re-rasterize) any bitmap assets for the new DPI or, optionally, bitmap stretch the currently loaded assets to the correct size.</span></span>
5.  <span data-ttu-id="e39ef-270">Grep para APIs que não são Per-Monitor DPI reconhecem e as substituem por Per-Monitor APIs com reconhecimento de DPI (quando aplicável).</span><span class="sxs-lookup"><span data-stu-id="e39ef-270">Grep for APIs that are not Per-Monitor DPI aware and replace them with Per-Monitor DPI-aware APIs (where applicable).</span></span> <span data-ttu-id="e39ef-271">Exemplo: substitua GetSystemMetrics por GetSystemMetricsForDpi.</span><span class="sxs-lookup"><span data-stu-id="e39ef-271">Example: replace GetSystemMetrics with GetSystemMetricsForDpi.</span></span>
6.  <span data-ttu-id="e39ef-272">Teste seu aplicativo em um sistema de várias exibições/vários DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-272">Test your application on a multiple-display/multi-DPI system.</span></span>
7.  <span data-ttu-id="e39ef-273">Para qualquer janela de nível superior em seu aplicativo que você não pode atualizar para a escala de DPI correta, use o dimensionamento de DPI de modo misto (descrito abaixo) para permitir o alargamento de bitmap dessas janelas de nível superior pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="e39ef-273">For any top-level windows in your application that you are unable to update to properly DPI scale, use mixed-mode DPI scaling (described below) to allow bitmap stretching of these top-level windows by the system.</span></span>

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a><span data-ttu-id="e39ef-274">Escala de DPI de Mixed-Mode (escala de PPP de subprocesso)</span><span class="sxs-lookup"><span data-stu-id="e39ef-274">Mixed-Mode DPI Scaling (Sub-Process DPI Scaling)</span></span>

<span data-ttu-id="e39ef-275">Ao atualizar um aplicativo para dar suporte ao reconhecimento de DPI por monitor, às vezes pode se tornar impraticável ou impossível atualizar cada janela no aplicativo em um só lugar.</span><span class="sxs-lookup"><span data-stu-id="e39ef-275">When updating an application to support per-monitor DPI awareness, it can sometimes become impractical or impossible to update every window in the application in one go.</span></span> <span data-ttu-id="e39ef-276">Isso pode ser simplesmente devido ao tempo e esforço necessários para atualizar e testar toda a interface do usuário, ou porque você não possui todo o código da interface do usuário que precisa ser executado (se seu aplicativo talvez carregue a interface do usuário de terceiros).</span><span class="sxs-lookup"><span data-stu-id="e39ef-276">This can simply be due to the time and effort required to update and test all UI, or because you do not own all of the UI code that you need to run (if your application perhaps loads third-party UI).</span></span> <span data-ttu-id="e39ef-277">Nessas situações, o Windows oferece uma maneira de facilitar o mundo da conscientização por monitor, permitindo que você execute algumas janelas de aplicativo (somente de nível superior) em seu modo original de reconhecimento de DPI enquanto você se concentra no seu tempo e na atualização de energia das partes mais importantes da sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e39ef-277">In these situations, Windows offers a way to ease into the world of per-monitor awareness by letting you run some of your application windows (top-level only) in their original DPI-awareness mode while you focus your time and energy updating the more important parts of your UI.</span></span>

<span data-ttu-id="e39ef-278">Veja abaixo uma ilustração de como isso poderia ser: você atualiza a interface do usuário do aplicativo principal ("janela principal" na ilustração) para executar com reconhecimento de DPI por monitor enquanto executa outras janelas em seu modo existente ("janela secundária").</span><span class="sxs-lookup"><span data-stu-id="e39ef-278">Below is an illustration of what this could look like: you update your main application UI ("Main Window"  in the illustration) to run with per-monitor DPI awareness while you run other windows in their existing mode ("Secondary Window").</span></span>

![diferenças no dimensionamento de DPI entre modos de reconhecimento](images/hub-page-illustrations.png)

<span data-ttu-id="e39ef-280">Antes da atualização de aniversário do Windows 10 (1607), o modo de reconhecimento de DPI de um processo era uma propriedade de todo o processo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-280">Prior to the Windows 10 Anniversary Update (1607), the DPI awareness mode of a process was a process-wide property.</span></span> <span data-ttu-id="e39ef-281">A partir da atualização de aniversário do Windows 10, essa propriedade agora pode ser definida por janela **de nível superior** .</span><span class="sxs-lookup"><span data-stu-id="e39ef-281">Beginning in the Windows 10 Anniversary Update, this property can now be set per **top-level** window.</span></span> <span data-ttu-id="e39ef-282">(O Windows **filho** deve continuar a corresponder ao tamanho de dimensionamento de seu pai.) Uma janela de nível superior é definida como uma janela sem nenhum pai.</span><span class="sxs-lookup"><span data-stu-id="e39ef-282">(**Child** windows must continue to match the scaling size of their parent.) A top-level window is defined as a window with no parent.</span></span> <span data-ttu-id="e39ef-283">Normalmente, essa é uma janela "regular" com os botões minimizar, maximizar e fechar.</span><span class="sxs-lookup"><span data-stu-id="e39ef-283">This is typically a "regular" window with minimize, maximize, and close buttons.</span></span> <span data-ttu-id="e39ef-284">O cenário para o qual o reconhecimento de DPI de subprocesso é destinado é ter a interface do usuário secundária dimensionada pelo Windows (bitmap ampliado) enquanto você concentra seu tempo e recursos na atualização da interface do usuário principal.</span><span class="sxs-lookup"><span data-stu-id="e39ef-284">The scenario that sub-process DPI awareness is intended for is to have secondary UI scaled by Windows (bitmap stretched) while you focus your time and resources on updating your primary UI.</span></span>

<span data-ttu-id="e39ef-285">Para habilitar o reconhecimento de DPI de subprocesso, chame [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) antes e depois de qualquer chamada de criação de janela.</span><span class="sxs-lookup"><span data-stu-id="e39ef-285">To enable sub-process DPI awareness, call [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) before and after any window creation calls.</span></span> <span data-ttu-id="e39ef-286">A janela criada será associada ao reconhecimento de DPI definido por meio de SetThreadDpiAwarenessContext.</span><span class="sxs-lookup"><span data-stu-id="e39ef-286">The window that is created will be associated with the DPI awareness that you set via SetThreadDpiAwarenessContext.</span></span> <span data-ttu-id="e39ef-287">Use a segunda chamada para restaurar o reconhecimento de DPI do thread s atual.</span><span class="sxs-lookup"><span data-stu-id="e39ef-287">Use the second call to restore the current thread s DPI awareness.</span></span>

<span data-ttu-id="e39ef-288">Embora o uso do dimensionamento de DPI de subprocesso permita que você confie no Windows para fazer parte do ajuste de DPI para seu aplicativo, ele pode aumentar a complexidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-288">While using sub-process DPI scaling enables you to rely on Windows to do some of the DPI scaling for your application, it can increase the complexity of your application.</span></span> <span data-ttu-id="e39ef-289">É importante entender as desvantagens dessa abordagem e da natureza das complexidades que ela apresenta.</span><span class="sxs-lookup"><span data-stu-id="e39ef-289">It is important that you understand the drawbacks of this approach and nature of the complexities that it introduces.</span></span> <span data-ttu-id="e39ef-290">Para obter mais informações sobre o reconhecimento de DPI de subprocesso, consulte [dimensionamento de dpi de modo misto e APIs com reconhecimento de DPI.](high-dpi-improvements-for-desktop-applications.md)</span><span class="sxs-lookup"><span data-stu-id="e39ef-290">For more information about sub-process DPI awareness, see [Mixed-Mode DPI Scaling and DPI-aware APIs.](high-dpi-improvements-for-desktop-applications.md)</span></span>

## <a name="testing-your-changes"></a><span data-ttu-id="e39ef-291">Testando suas alterações</span><span class="sxs-lookup"><span data-stu-id="e39ef-291">Testing Your Changes</span></span>

<span data-ttu-id="e39ef-292">Depois de atualizar seu aplicativo para se tornar um reconhecimento de DPI por monitor, é importante validar seu aplicativo corretamente responde às alterações de DPI em um ambiente de DPI misto.</span><span class="sxs-lookup"><span data-stu-id="e39ef-292">After you have updated your application to become per-monitor DPI aware, it is important to validate your application properly responds to DPI changes in a mixed-DPI environment.</span></span> <span data-ttu-id="e39ef-293">Algumas especificidades para teste incluem:</span><span class="sxs-lookup"><span data-stu-id="e39ef-293">Some specifics to test include:</span></span>

1.  <span data-ttu-id="e39ef-294">Mover janelas de aplicativos para frente e para trás entre telas de valores de DPI diferentes</span><span class="sxs-lookup"><span data-stu-id="e39ef-294">Moving application windows back and forth between displays of different DPI values</span></span>
2.  <span data-ttu-id="e39ef-295">Iniciando seu aplicativo em exibições de valores de DPI diferentes</span><span class="sxs-lookup"><span data-stu-id="e39ef-295">Starting your application on displays of different DPI values</span></span>
3.  <span data-ttu-id="e39ef-296">Alterando o fator de escala para o monitor enquanto o aplicativo está em execução</span><span class="sxs-lookup"><span data-stu-id="e39ef-296">Changing the scale factor for your monitor while the application is running</span></span>
4.  <span data-ttu-id="e39ef-297">Alterar a exibição que você usa como a exibição primária, _sair do Windows_ e, em seguida, testar novamente seu aplicativo depois de entrar novamente.</span><span class="sxs-lookup"><span data-stu-id="e39ef-297">Changing the display that you use as the primary display, _signing out of Windows_, then re-testing your application after signing back in.</span></span> <span data-ttu-id="e39ef-298">Isso é particularmente útil na localização de código que usa dimensões/tamanhos embutidos em código.</span><span class="sxs-lookup"><span data-stu-id="e39ef-298">This is particularly useful in finding code that uses hard-coded sizes/dimensions.</span></span>

## <a name="common-pitfalls-win32"></a><span data-ttu-id="e39ef-299">Armadilhas comuns (Win32)</span><span class="sxs-lookup"><span data-stu-id="e39ef-299">Common Pitfalls (Win32)</span></span>

<span data-ttu-id="e39ef-300">**Não está usando o retângulo sugerido que é fornecido no WM \_ DPICHANGED**</span><span class="sxs-lookup"><span data-stu-id="e39ef-300">**Not using the suggested rectangle that is provided in WM\_DPICHANGED**</span></span>

<span data-ttu-id="e39ef-301">Quando o Windows envia a janela do aplicativo a uma mensagem do [**WM \_ DPICHANGED**](wm-dpichanged.md) , essa mensagem inclui um retângulo sugerido que você deve usar para redimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="e39ef-301">When Windows sends your application window a [**WM\_DPICHANGED**](wm-dpichanged.md) message, this message includes a suggested rectangle that you should use to resize your window.</span></span> <span data-ttu-id="e39ef-302">É fundamental que seu aplicativo use esse retângulo para se redimensionar, como isso irá:</span><span class="sxs-lookup"><span data-stu-id="e39ef-302">It is critical that your application use this rectangle to resize itself, as this will:</span></span>

1.  <span data-ttu-id="e39ef-303">Verifique se o cursor do mouse permanecerá na mesma posição relativa na janela ao arrastar entre exibições</span><span class="sxs-lookup"><span data-stu-id="e39ef-303">Ensure that the mouse cursor will stay in the same relative position on the Window when dragging between displays</span></span>
2.  <span data-ttu-id="e39ef-304">Impedir que a janela do aplicativo entre em um ciclo de alteração de DPI recursivo em que uma alteração de DPI disparará uma alteração de DPI subsequente, que disparará ainda outra alteração de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-304">Prevent the application window from getting into a recursive dpi-change cycle where one DPI change triggers a subsequent DPI change, which triggers yet another DPI change.</span></span>

<span data-ttu-id="e39ef-305">Se você tiver requisitos específicos do aplicativo que impedem o uso do retângulo sugerido que o Windows fornece na \_ mensagem do WM DPICHANGED, consulte [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span><span class="sxs-lookup"><span data-stu-id="e39ef-305">If you have application-specific requirements that prevent you from using the suggested rectangle that Windows provides in the WM\_DPICHANGED message, see [**WM\_GETDPISCALEDSIZE**](wm-getdpiscaledsize.md).</span></span> <span data-ttu-id="e39ef-306">Essa mensagem pode ser usada para dar ao Windows um tamanho desejado que você gostaria de usar depois que a alteração de DPI ocorreu, enquanto ainda evitava os problemas descritos acima.</span><span class="sxs-lookup"><span data-stu-id="e39ef-306">This message can be used to give Windows a desired size you'd like used once the DPI change has occurred, while still avoiding the issues described above.</span></span>

<span data-ttu-id="e39ef-307">**Falta de documentação sobre virtualização**</span><span class="sxs-lookup"><span data-stu-id="e39ef-307">**Lack of documentation about virtualization**</span></span>

<span data-ttu-id="e39ef-308">Quando um HWND ou processo está sendo executado como um DPI ou reconhecimento de DPI do sistema, ele pode ser bitmap ampliado pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="e39ef-308">When an HWND or process is running as either DPI unaware or system DPI aware, it can be bitmap stretched by Windows.</span></span> <span data-ttu-id="e39ef-309">Quando isso acontece, o Windows dimensiona e converte informações sensíveis a DPI de algumas APIs para o espaço de coordenadas do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="e39ef-309">When this happens, Windows scales and converts DPI-sensitive information from some APIs to the coordinate space of the calling thread.</span></span> <span data-ttu-id="e39ef-310">Por exemplo, se um thread sem reconhecimento de DPI consultar o tamanho da tela durante a execução em uma exibição de alto DPI, o Windows virtualizará a resposta fornecida para o aplicativo como se a tela estivesse em unidades de 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-310">For example, if a DPI-unaware thread queries the screen size while running on a high-DPI display, Windows will virtualize the answer given to the application as if the screen were in 96 DPI units.</span></span> <span data-ttu-id="e39ef-311">Como alternativa, quando um thread com reconhecimento de DPI do sistema está interagindo com uma exibição em um DPI diferente do que estava em uso quando a sessão do usuário atual foi iniciada, o Windows irá dimensionar em DPI algumas chamadas à API para o espaço de coordenadas que o HWND usaria se estivesse em execução em seu fator de escala de DPI original.</span><span class="sxs-lookup"><span data-stu-id="e39ef-311">Alternatively, when a System DPI-aware thread is interacting with a display at a different DPI than was in use when the current user's session was started, Windows will DPI-scale some API calls into the coordinate space that the HWND would be using if it were running at its original DPI scale factor.</span></span>

<span data-ttu-id="e39ef-312">Quando você atualiza seu aplicativo de desktop para a escala de DPI corretamente, pode ser difícil saber quais chamadas de API podem retornar valores virtualizados com base no contexto do thread; Atualmente, essas informações não estão suficientemente documentadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e39ef-312">When you update your desktop application to DPI scale properly, it can difficult to know which API calls can return virtualized values based on the thread context; this information is not currently sufficiently documented by Microsoft.</span></span> <span data-ttu-id="e39ef-313">Lembre-se de que se você chamar qualquer API do sistema de um contexto de thread com reconhecimento de DPI ou sistema, o valor de retorno poderá ser virtualizado.</span><span class="sxs-lookup"><span data-stu-id="e39ef-313">Be aware that if you call any system API from a DPI-unaware or system-DPI-aware thread context, the return value might be virtualized.</span></span> <span data-ttu-id="e39ef-314">Dessa forma, verifique se o thread está em execução no contexto de DPI que você espera ao interagir com a tela ou com janelas individuais.</span><span class="sxs-lookup"><span data-stu-id="e39ef-314">As such, make sure your thread is running in the DPI context you expect when interacting with the screen or individual windows.</span></span> <span data-ttu-id="e39ef-315">Ao alterar temporariamente o contexto de DPI de um thread usando [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), certifique-se de restaurar o contexto antigo quando terminar de evitar causar um comportamento incorreto em outro lugar em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-315">When temporarily changing a thread's DPI context using [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), be sure to restore the old context when you're done to avoid causing incorrect behavior elsewhere in your application.</span></span>

<span data-ttu-id="e39ef-316">**Muitas APIs do Windows não têm um contexto de DPI**</span><span class="sxs-lookup"><span data-stu-id="e39ef-316">**Many Windows APIs do not have an DPI context**</span></span>

<span data-ttu-id="e39ef-317">Muitas APIs herdadas do Windows não incluem um contexto de DPI ou HWND como parte de sua interface.</span><span class="sxs-lookup"><span data-stu-id="e39ef-317">Many legacy Windows APIs do not include a DPI or HWND context as part of their interface.</span></span> <span data-ttu-id="e39ef-318">Como resultado, os desenvolvedores geralmente precisam realizar trabalho adicional para lidar com o dimensionamento de qualquer informação sensível a DPI, como tamanhos, pontos ou ícones.</span><span class="sxs-lookup"><span data-stu-id="e39ef-318">As a result, developers often have to do additional work to handle the scaling of any DPI-sensitive information, such as sizes, points, or icons.</span></span> <span data-ttu-id="e39ef-319">Por exemplo, os desenvolvedores que usam [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) devem bitmaps de Stretch ou usar APIs alternativas para carregar ícones de tamanho correto para o DPI apropriado, como [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span><span class="sxs-lookup"><span data-stu-id="e39ef-319">As an example, developers using [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) must either bitmap stretch loaded icons or use alternate APIs to load correctly-sized icons for the appropriate DPI, such as [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).</span></span>

<span data-ttu-id="e39ef-320">**Redefinição forçada do reconhecimento de DPI em todo o processo**</span><span class="sxs-lookup"><span data-stu-id="e39ef-320">**Forced reset of process-wide DPI awareness**</span></span>

<span data-ttu-id="e39ef-321">Em geral, o modo de reconhecimento de DPI do seu processo não pode ser alterado após a inicialização do processo.</span><span class="sxs-lookup"><span data-stu-id="e39ef-321">In general, the DPI awareness mode of your process cannot be changed after process initialization.</span></span> <span data-ttu-id="e39ef-322">No entanto, o Windows pode alterar forçosamente o modo de reconhecimento de DPI do seu processo se você tentar interromper o requisito de que todos os HWNDs em uma árvore de janela tenham o mesmo modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-322">Windows can, however, forcibly change the DPI awareness mode of your process if you attempt to break the requirement that all HWNDs in a window tree have the same DPI awareness mode.</span></span> <span data-ttu-id="e39ef-323">Em todas as versões do Windows, a partir do Windows 10 1703, não é possível ter diferentes HWNDs em uma árvore HWND executada em modos de reconhecimento de DPI diferentes.</span><span class="sxs-lookup"><span data-stu-id="e39ef-323">On all versions of Windows, as of Windows 10 1703, it is not possible to have different HWNDs in an HWND tree run in different DPI awareness modes.</span></span> <span data-ttu-id="e39ef-324">Se você tentar criar uma relação filho-pai que interrompa essa regra, o reconhecimento de DPI do processo inteiro poderá ser redefinido.</span><span class="sxs-lookup"><span data-stu-id="e39ef-324">If you attempt to create a child-parent relationship that breaks this rule, the DPI awareness of the entire process can be reset.</span></span> <span data-ttu-id="e39ef-325">Isso pode ser disparado por:</span><span class="sxs-lookup"><span data-stu-id="e39ef-325">This can be triggered by:</span></span>

1.  <span data-ttu-id="e39ef-326">Uma chamada CreateWindow em que a janela pai passada é de um modo de reconhecimento de DPI diferente do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="e39ef-326">A CreateWindow call where the passed in parent window is of a different DPI awareness mode than the calling thread.</span></span>
2.  <span data-ttu-id="e39ef-327">Uma chamada setpai em que as duas janelas estão associadas a modos de reconhecimento de DPI diferentes.</span><span class="sxs-lookup"><span data-stu-id="e39ef-327">A SetParent call where the two windows are associated with different DPI awareness modes.</span></span>

<span data-ttu-id="e39ef-328">A tabela a seguir mostra o que acontece se você tentar violar esta regra:</span><span class="sxs-lookup"><span data-stu-id="e39ef-328">The table below shows what happens if you attempt to violate this rule:</span></span>



| <span data-ttu-id="e39ef-329">Operação</span><span class="sxs-lookup"><span data-stu-id="e39ef-329">Operation</span></span>                 | <span data-ttu-id="e39ef-330">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e39ef-330">Windows 8.1</span></span>                                  | <span data-ttu-id="e39ef-331">Windows 10 (1607 e anterior)</span><span class="sxs-lookup"><span data-stu-id="e39ef-331">Windows 10 (1607 and earlier)</span></span>                | <span data-ttu-id="e39ef-332">Windows 10 (1703 e posterior)</span><span class="sxs-lookup"><span data-stu-id="e39ef-332">Windows 10 (1703 and later)</span></span>                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| <span data-ttu-id="e39ef-333">CreateWindow (em processo)</span><span class="sxs-lookup"><span data-stu-id="e39ef-333">CreateWindow (In-Proc)</span></span>    | <span data-ttu-id="e39ef-334">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-334">N/A</span></span>                                          | <span data-ttu-id="e39ef-335">**Heranças filho** (modo misto)</span><span class="sxs-lookup"><span data-stu-id="e39ef-335">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="e39ef-336">**Heranças filho** (modo misto)</span><span class="sxs-lookup"><span data-stu-id="e39ef-336">**Child inherits** (mixed mode)</span></span>              |
| <span data-ttu-id="e39ef-337">CreateWindow (proc cruzado)</span><span class="sxs-lookup"><span data-stu-id="e39ef-337">CreateWindow (Cross-Proc)</span></span> | <span data-ttu-id="e39ef-338">**Redefinição forçada** (do processo do chamador)</span><span class="sxs-lookup"><span data-stu-id="e39ef-338">**Forced reset** (of caller's process)</span></span>       | <span data-ttu-id="e39ef-339">**Heranças filho** (modo misto)</span><span class="sxs-lookup"><span data-stu-id="e39ef-339">**Child inherits** (mixed mode)</span></span>              | <span data-ttu-id="e39ef-340">**Redefinição forçada** (do processo do chamador)</span><span class="sxs-lookup"><span data-stu-id="e39ef-340">**Forced reset** (of caller's process)</span></span>       |
| <span data-ttu-id="e39ef-341">Setpai (no processo)</span><span class="sxs-lookup"><span data-stu-id="e39ef-341">SetParent (In-Proc)</span></span>       | <span data-ttu-id="e39ef-342">N/D</span><span class="sxs-lookup"><span data-stu-id="e39ef-342">N/A</span></span>                                          | <span data-ttu-id="e39ef-343">**Redefinição forçada** (do processo atual)</span><span class="sxs-lookup"><span data-stu-id="e39ef-343">**Forced reset** (of current process)</span></span>        | <span data-ttu-id="e39ef-344">**Falha** ( \_ estado inválido do erro \_ )</span><span class="sxs-lookup"><span data-stu-id="e39ef-344">**Fail** (ERROR\_INVALID\_STATE)</span></span>             |
| <span data-ttu-id="e39ef-345">Setpai (proc cruzado)</span><span class="sxs-lookup"><span data-stu-id="e39ef-345">SetParent (Cross-Proc)</span></span>    | <span data-ttu-id="e39ef-346">**Redefinição forçada** (do processo da janela filho)</span><span class="sxs-lookup"><span data-stu-id="e39ef-346">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="e39ef-347">**Redefinição forçada** (do processo da janela filho)</span><span class="sxs-lookup"><span data-stu-id="e39ef-347">**Forced reset** (of child window's process)</span></span> | <span data-ttu-id="e39ef-348">**Redefinição forçada** (do processo da janela filho)</span><span class="sxs-lookup"><span data-stu-id="e39ef-348">**Forced reset** (of child window's process)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e39ef-349">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e39ef-349">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e39ef-350">Referência de API de DPI alta</span><span class="sxs-lookup"><span data-stu-id="e39ef-350">High DPI API Reference</span></span>](high-dpi-reference.md)
</dt> <dt>

[<span data-ttu-id="e39ef-351">Dimensionamento de DPI de modo misto e APIs com reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e39ef-351">Mixed-Mode DPI Scaling and DPI-aware APIs.</span></span>](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

