---
title: Desenvolver um aplicativo WPF com reconhecimento de DPI por monitor
description: Observação Esta página aborda o desenvolvimento WPF herdado para Windows 8.1. Se você estiver desenvolvendo aplicativos do WPF para o Windows 10, consulte a documentação mais recente no GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interface do usuário do Windows, aplicativos com reconhecimento de DPI
- Interface do usuário do Windows, DPI alto
- Aplicativos com reconhecimento de DPI
- DPI alto
- Escrevendo aplicativos Win32 com reconhecimento de DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084543"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="5aeff-110">Desenvolver um aplicativo WPF com reconhecimento de DPI por monitor</span><span class="sxs-lookup"><span data-stu-id="5aeff-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="5aeff-111">**APIs importantes**</span><span class="sxs-lookup"><span data-stu-id="5aeff-111">**Important APIs**</span></span>

-   [<span data-ttu-id="5aeff-112">**SetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="5aeff-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="5aeff-113">**GetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="5aeff-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="5aeff-114">**GetDpiForMonitor**</span><span class="sxs-lookup"><span data-stu-id="5aeff-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="5aeff-115">**Esta página aborda o desenvolvimento WPF herdado para Windows 8.1.**</span><span class="sxs-lookup"><span data-stu-id="5aeff-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="5aeff-116">Se você estiver desenvolvendo aplicativos do WPF para o Windows 10, consulte a <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentação mais recente no github.</a></span><span class="sxs-lookup"><span data-stu-id="5aeff-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="5aeff-117">O Windows 8.1 oferece aos desenvolvedores novas funcionalidades para criar aplicativos de área de trabalho que reconhecem o DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="5aeff-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="5aeff-118">Para aproveitar essa funcionalidade, um aplicativo com reconhecimento de DPI por monitor deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5aeff-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="5aeff-119">Alterar as dimensões da janela para manter um tamanho físico que pareça consistente em qualquer exibição</span><span class="sxs-lookup"><span data-stu-id="5aeff-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="5aeff-120">Refazer layout e renderizar novamente os gráficos para o novo tamanho da janela</span><span class="sxs-lookup"><span data-stu-id="5aeff-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="5aeff-121">Selecionar as fontes que são dimensionadas adequadamente para o nível de DPI</span><span class="sxs-lookup"><span data-stu-id="5aeff-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="5aeff-122">Selecionar e carregar ativos de bitmap que são personalizados para o nível de DPI</span><span class="sxs-lookup"><span data-stu-id="5aeff-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="5aeff-123">Para facilitar a criação de um aplicativo com reconhecimento de DPI por monitor, o Windows 8.1 fornece o seguinte Win32APIs da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="5aeff-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="5aeff-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (ou entrada de manifesto de DPI) define o processo para um nível de reconhecimento de DPI especificado, que determina como o Windows dimensiona a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="5aeff-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="5aeff-125">Isso substitui [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="5aeff-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="5aeff-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) retorna o nível de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="5aeff-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="5aeff-127">Isso substitui [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="5aeff-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="5aeff-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) retorna o DPI de um monitor.</span><span class="sxs-lookup"><span data-stu-id="5aeff-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="5aeff-129">A notificação da janela do [**WM \_ DPICHANGED**](wm-dpichanged.md) é enviada para aplicativos com reconhecimento de DPI por monitor quando a posição de uma janela é alterada de modo que a maior parte de sua área cruza um monitor com um DPI diferente do DPI antes da alteração da posição ou quando o usuário move o controle deslizante de exibição.</span><span class="sxs-lookup"><span data-stu-id="5aeff-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="5aeff-130">Para criar um aplicativo que seja redimensionado e renderizado novamente quando um usuário o mover para uma exibição diferente, use essa notificação.</span><span class="sxs-lookup"><span data-stu-id="5aeff-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="5aeff-131">Para obter mais detalhes sobre vários níveis de reconhecimento de DPI com suporte para aplicativos de área de trabalho no Windows 8.1 consulte o tópico [escrevendo DPI-Aware desktop e aplicativos Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="5aeff-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="5aeff-132">Escala de DPI e WPF</span><span class="sxs-lookup"><span data-stu-id="5aeff-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="5aeff-133">Os aplicativos Windows Presentation Foundation (WPF) são, por padrão, reconhecem o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="5aeff-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="5aeff-134">Para obter definições dos diferentes níveis de reconhecimento de DPI, consulte o tópico [escrevendo DPI-Aware aplicativos de área de trabalho e Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="5aeff-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="5aeff-135">O sistema de gráficos do WPF usa unidades independentes de dispositivo para habilitar a resolução e a independência do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5aeff-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="5aeff-136">O WPF dimensiona cada pixel independente de dispositivo automaticamente com base no DPI atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="5aeff-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="5aeff-137">Isso permite que os aplicativos do WPF sejam dimensionados automaticamente quando a DPI do monitor em que a janela está estiver no mesmo DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="5aeff-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="5aeff-138">No entanto, como os aplicativos WPF são reconhecendo o DPI do sistema, o aplicativo será dimensionado pelo sistema operacional quando o aplicativo for movido para um monitor com um DPI diferente ou quando o controle deslizante no painel de controle for usado para alterar o DPI.</span><span class="sxs-lookup"><span data-stu-id="5aeff-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="5aeff-139">O dimensionamento no sistema operacional pode fazer com que os aplicativos WPF pareçam borrados, especialmente quando o dimensionamento é não integral.</span><span class="sxs-lookup"><span data-stu-id="5aeff-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="5aeff-140">Para evitar o dimensionamento de aplicativos do WPF, eles precisam ser atualizados para que haja reconhecimento de DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="5aeff-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="5aeff-141">Instruções de exemplo de WPF de acordo com reconhecimento de monitor</span><span class="sxs-lookup"><span data-stu-id="5aeff-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="5aeff-142">O [exemplo de WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) é um aplicativo WPF de exemplo atualizado para ser compatível com dpi por monitor.</span><span class="sxs-lookup"><span data-stu-id="5aeff-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="5aeff-143">O exemplo consiste em dois projetos:</span><span class="sxs-lookup"><span data-stu-id="5aeff-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="5aeff-144">NativeHelpers. vcxproj: Este é um projeto auxiliar nativo que implementa a funcionalidade básica para criar um aplicativo WPF como reconhecimento de DPI por monitor utilizando o Win32APIs acima.</span><span class="sxs-lookup"><span data-stu-id="5aeff-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="5aeff-145">O projeto contém duas classes:</span><span class="sxs-lookup"><span data-stu-id="5aeff-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="5aeff-146">PerMonDPIHelpers: uma classe que fornece funções auxiliares para operações relacionadas a DPI, como recuperar o DPI atual do monitor ativo, definindo um processo para ser compatível com DPI por meio do monitor, etc.</span><span class="sxs-lookup"><span data-stu-id="5aeff-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="5aeff-147">PerMonitorDPIWindow: uma classe base derivada de **System. Windows. Window** que implementa a funcionalidade para fazer com que uma janela do aplicativo WPF seja compatível com dpi por monitor.</span><span class="sxs-lookup"><span data-stu-id="5aeff-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="5aeff-148">Ajusta o tamanho da janela, o tamanho da renderização de gráficos e o tamanho da fonte com base no DPI do monitor em vez do DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="5aeff-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="5aeff-149">WPFApplication. csproj: aplicativo de exemplo do WPF que consome o PerMonitorDPIWindow (PerMonitorDPIWindow) e mostra como a janela do aplicativo e a renderização são redimensionadas quando a janela é movida para um monitor com um DPI diferente ou quando o controle deslizante no painel de controle de exibição é usado para alterar o DPI.</span><span class="sxs-lookup"><span data-stu-id="5aeff-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="5aeff-150">Para executar o exemplo, siga as etapas abaixo:</span><span class="sxs-lookup"><span data-stu-id="5aeff-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="5aeff-151">Baixar e descompactar o [exemplo de WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span><span class="sxs-lookup"><span data-stu-id="5aeff-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="5aeff-152">Iniciar Microsoft Visual Studio e selecionar **arquivo > abrir > projeto/solução**</span><span class="sxs-lookup"><span data-stu-id="5aeff-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="5aeff-153">Navegue até o diretório que contém o exemplo descompactado.</span><span class="sxs-lookup"><span data-stu-id="5aeff-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="5aeff-154">Vá para o diretório chamado para o exemplo e clique duas vezes no arquivo da solução do Visual Studio (. sln)</span><span class="sxs-lookup"><span data-stu-id="5aeff-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="5aeff-155">Pressione F7 ou use **compilar > Compilar solução** para criar o exemplo</span><span class="sxs-lookup"><span data-stu-id="5aeff-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="5aeff-156">Pressione CTRL + F5 ou use **Debug > iniciar sem depuração** para executar o exemplo</span><span class="sxs-lookup"><span data-stu-id="5aeff-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="5aeff-157">Para ver o impacto da alteração de DPI em um aplicativo do WPF que é atualizado para ter reconhecimento de DPI por monitor usando a classe base no exemplo, mova a janela do aplicativo para e de exibições que tenham DPIs diferentes.</span><span class="sxs-lookup"><span data-stu-id="5aeff-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="5aeff-158">À medida que a janela é movida entre monitores, o tamanho da janela e a escala da interface do usuário são atualizados com base no DPI da exibição usando o sistema gráfico escalonável do WPF, em vez de ser dimensionado pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5aeff-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="5aeff-159">A interface do usuário do aplicativo é renderizada nativamente e não aparece borrada.</span><span class="sxs-lookup"><span data-stu-id="5aeff-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="5aeff-160">Se você não tiver dois monitores com DPI diferente, altere o DPI alterando o controle deslizante no painel de controle de exibição.</span><span class="sxs-lookup"><span data-stu-id="5aeff-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="5aeff-161">Alterar o controle deslizante e clicar em **aplicar** redimensionará a janela do aplicativo e atualizará a escala da interface do usuário automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5aeff-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="5aeff-162">Atualizando um aplicativo existente do WPF para ter reconhecimento de DPI por monitor usando o projeto auxiliar no exemplo do WPF</span><span class="sxs-lookup"><span data-stu-id="5aeff-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="5aeff-163">Se você tiver um aplicativo existente do WPF e desejar aproveitar o projeto auxiliar de DPI do exemplo para torná-lo ciente de DPI, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="5aeff-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="5aeff-164">Baixar e descompactar o exemplo de WPF com reconhecimento de monitor</span><span class="sxs-lookup"><span data-stu-id="5aeff-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="5aeff-165">Inicie o Visual Studio e selecione **arquivo > abrir > projeto/solução**</span><span class="sxs-lookup"><span data-stu-id="5aeff-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="5aeff-166">Navegue até o diretório que contém um aplicativo existente do WPF e clique duas vezes no arquivo da solução do Visual Studio (. sln)</span><span class="sxs-lookup"><span data-stu-id="5aeff-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="5aeff-167">Clique com o botão direito do mouse em **solução > adicionar > projeto existente** ![ uma captura de tela que ilustra a seleção de menu Adicionar: projeto existente](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="5aeff-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="5aeff-168">Na caixa de diálogo seleção de arquivo, navegue até o diretório que contém o exemplo descompactado.</span><span class="sxs-lookup"><span data-stu-id="5aeff-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="5aeff-169">Abra o diretório chamado para o exemplo, navegue até a pasta "NativeHelpers", selecione o arquivo de projeto Visual C++ "NativeHelpers. vcxproj" e clique em **OK**</span><span class="sxs-lookup"><span data-stu-id="5aeff-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="5aeff-170">Clique com o botão direito do mouse no projeto NativeHelpers e selecione **Compilar**.</span><span class="sxs-lookup"><span data-stu-id="5aeff-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="5aeff-171">Isso irá gerar NativeHelpers.dll que serão adicionadas como uma referência ao aplicativo do WPF na próxima etapa ![ uma captura de tela ilustrando a seleção do menu Build](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="5aeff-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="5aeff-172">Adicione uma referência a NativeHelpers.dll de seu aplicativo WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="5aeff-173">Expanda seu projeto de aplicativo WPF, clique com o botão direito do mouse em **referências** e clique em **Adicionar referência..** .</span><span class="sxs-lookup"><span data-stu-id="5aeff-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="5aeff-174">Na caixa de diálogo resultante, expanda a seção **solução** .</span><span class="sxs-lookup"><span data-stu-id="5aeff-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="5aeff-175">Em **projetos**, selecione NativeHelpers e clique em **OK** ![ uma captura de tela ilustrando a caixa de diálogo do Resource Manager](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="5aeff-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="5aeff-176">Expanda seu projeto de aplicativo WPF, expanda **Propriedades** e abra **AssemblyInfo. cs**.</span><span class="sxs-lookup"><span data-stu-id="5aeff-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="5aeff-177">Faça as seguintes adições ao AssemblyInfo. cs</span><span class="sxs-lookup"><span data-stu-id="5aeff-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="5aeff-178">Adicione referência a System. Windows. Media na seção de referência (usando System. Windows. Media;)</span><span class="sxs-lookup"><span data-stu-id="5aeff-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="5aeff-179">Adicionar o atributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )</span><span class="sxs-lookup"><span data-stu-id="5aeff-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![uma captura de tela que ilustra as propriedades adicionais](images/scrvs-image4.png)
10. <span data-ttu-id="5aeff-181">Herdar a classe de janela principal do WPF da classe base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="5aeff-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="5aeff-182">Atualize o arquivo. cs da janela principal do WPF para herdar da classe base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="5aeff-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="5aeff-183">Adicione uma referência a NativeHelpers na seção de referência adicionando a linha `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="5aeff-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="5aeff-184">Herdar a classe de janela principal da classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="5aeff-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![uma captura de tela ilustrando a referência do c++](images/scrvs-image5.png)
    -   <span data-ttu-id="5aeff-186">Atualize o arquivo. XAML da janela principal do WPF para herdar da classe base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="5aeff-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="5aeff-187">Adicione uma referência a NativeHelpers na seção de referência adicionando a linha `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="5aeff-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="5aeff-188">Herdar a classe de janela principal da classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="5aeff-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![uma captura de tela ilustrando a adição da referência. XAML](images/scrvs-image6.png)
11. <span data-ttu-id="5aeff-190">Pressione F7 ou use **compilar > Compilar solução** para criar o exemplo</span><span class="sxs-lookup"><span data-stu-id="5aeff-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="5aeff-191">Pressione CTRL + F5 ou use **Debug > iniciar sem depuração** para executar o exemplo</span><span class="sxs-lookup"><span data-stu-id="5aeff-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="5aeff-192">O aplicativo de [exemplo do WPF com reconhecimento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) ilustra como um aplicativo do WPF pode ser atualizado para que haja reconhecimento de DPI por monitor respondendo à notificação da janela [**\_ DPICHANGED do WM**](wm-dpichanged.md) .</span><span class="sxs-lookup"><span data-stu-id="5aeff-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="5aeff-193">Em resposta à notificação de janela, o exemplo atualiza a transformação de escala usada pelo WPF com base no DPI atual do monitor em que a janela está.</span><span class="sxs-lookup"><span data-stu-id="5aeff-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="5aeff-194">O *wParam* da notificação de janela contém o novo dpi no *wParam*.</span><span class="sxs-lookup"><span data-stu-id="5aeff-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="5aeff-195">O *lParam* contém um retângulo que tem o tamanho e a posição da nova janela sugerida, dimensionada para o novo dpi.</span><span class="sxs-lookup"><span data-stu-id="5aeff-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="5aeff-196">Observação:</span><span class="sxs-lookup"><span data-stu-id="5aeff-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="5aeff-197">Como este exemplo substitui o tamanho da janela e a transformação de escala do nó raiz da janela do WPF, o trabalho adicional pode ser exigido pelo desenvolvedor do aplicativo se:</span><span class="sxs-lookup"><span data-stu-id="5aeff-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="5aeff-198">O tamanho da janela afeta outras partes do aplicativo como esta janela do WPF sendo hospedada dentro de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5aeff-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="5aeff-199">O aplicativo WPF que está estendendo essa classe está definindo outra transformação no Visual raiz; o exemplo pode substituir alguma outra transformação que está sendo aplicada pelo próprio aplicativo WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="5aeff-200">Visão geral do projeto auxiliar no exemplo do WPF</span><span class="sxs-lookup"><span data-stu-id="5aeff-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="5aeff-201">Para tornar um aplicativo existente do WPF por monitor com reconhecimento de DPI, a biblioteca NativeHelpers fornece a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="5aeff-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="5aeff-202">**Marca o aplicativo WPF como reconhecimento de DPI por ponitor:** O aplicativo do WPF é marcado como reconhecimento de DPI por monitor chamando [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="5aeff-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="5aeff-203">Marcar o aplicativo como reconhecimento de DPI por monitor garantirá que</span><span class="sxs-lookup"><span data-stu-id="5aeff-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="5aeff-204">O sistema operacional não dimensiona o aplicativo quando o DPI do sistema não corresponde ao DPI atual do monitor em que a janela do aplicativo está</span><span class="sxs-lookup"><span data-stu-id="5aeff-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="5aeff-205">A mensagem do [**WM \_ DPICHANGED**](wm-dpichanged.md) é enviada sempre que o DPI da janela é alterado</span><span class="sxs-lookup"><span data-stu-id="5aeff-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="5aeff-206">**Ajusta a dimensão da janela, refazer o layout e renderizar novamente o conteúdo de gráficos e selecionar fontes com base no dpi inicial do monitor em que a janela está:** Depois que o aplicativo for marcado como com reconhecimento de DPI por monitor, o WPF ainda dimensionará o tamanho da janela, os gráficos e o tamanho da fonte com base no DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="5aeff-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="5aeff-207">Desde que, na inicialização do aplicativo, não há garantia de que o DPI do sistema seja o mesmo que o DPI do monitor em que a janela é iniciada, a biblioteca ajusta esses valores depois que a janela é carregada.</span><span class="sxs-lookup"><span data-stu-id="5aeff-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="5aeff-208">A classe base **PerMonitorDPIWindow** as atualiza no manipulador **OnLoaded ()** .</span><span class="sxs-lookup"><span data-stu-id="5aeff-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="5aeff-209">O tamanho da janela é atualizado alterando as propriedades **Width** e **Height** da janela.</span><span class="sxs-lookup"><span data-stu-id="5aeff-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="5aeff-210">O layout e o tamanho são atualizados com a aplicação de uma transformação de escala apropriada ao nó raiz da janela do WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="5aeff-211">**Responde ao WM \_ Notificação da janela DPICHANGED:** atualize o tamanho da janela, os gráficos e o tamanho da fonte com base no dpi passado na notificação da janela.</span><span class="sxs-lookup"><span data-stu-id="5aeff-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="5aeff-212">A classe base **PerMonitorDPIWindow** manipula a notificação de janela no método **HandleMessages ()** .</span><span class="sxs-lookup"><span data-stu-id="5aeff-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="5aeff-213">O tamanho da janela é atualizado chamando **SetWindowPos** usando as informações passadas no *lParam* da mensagem da janela.</span><span class="sxs-lookup"><span data-stu-id="5aeff-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="5aeff-214">O layout e o tamanho dos gráficos são atualizados com a aplicação de uma transformação de escala apropriada ao nó raiz da janela do WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="5aeff-215">O fator de escala é calculado usando o DPI passado no *wParam* da mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="5aeff-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="5aeff-216">Tratamento de alteração de DPI para ativos como imagens</span><span class="sxs-lookup"><span data-stu-id="5aeff-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="5aeff-217">Para atualizar o conteúdo de gráficos, o aplicativo WPF de exemplo aplica uma transformação de escala ao nó raiz do aplicativo do WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="5aeff-218">Embora isso funcione bem para o conteúdo que é processado nativamente pelo WPF (Rectangle, Text etc.), isso implica que os ativos de bitmap, como as imagens, são dimensionados pelo WPF.</span><span class="sxs-lookup"><span data-stu-id="5aeff-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="5aeff-219">Para evitar bitmaps borrados causados pelo dimensionamento, o desenvolvedor de aplicativos do WPF pode gravar um controle de imagem de DPI personalizado que seleciona um ativo diferente com base na DPI atual do monitor em que a janela está.</span><span class="sxs-lookup"><span data-stu-id="5aeff-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="5aeff-220">O controle de imagem pode contar com o evento **DPIChanged ()** disparado para a janela do WPF que consome do **PerMonitorDPIWindow**, quando o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="5aeff-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="5aeff-221">O controle de imagem também deve selecionar o controle certo durante a inicialização do aplicativo no manipulador de eventos de janela do WPF **carregado ()** .</span><span class="sxs-lookup"><span data-stu-id="5aeff-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 