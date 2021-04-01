---
title: DPI e Device-Independent pixels
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Saiba mais sobre: DPI e Device-Independent pixels'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837210"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="d4d12-103">DPI e Device-Independent pixels</span><span class="sxs-lookup"><span data-stu-id="d4d12-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="d4d12-104">Para programar com eficiência com gráficos do Windows, você deve entender dois conceitos relacionados:</span><span class="sxs-lookup"><span data-stu-id="d4d12-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="d4d12-105">Pontos por polegada (DPI)</span><span class="sxs-lookup"><span data-stu-id="d4d12-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="d4d12-106">Pixel independente de dispositivo (DIPs).</span><span class="sxs-lookup"><span data-stu-id="d4d12-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="d4d12-107">Vamos começar com DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-107">Let's start with DPI.</span></span> <span data-ttu-id="d4d12-108">Isso exigirá um breve desvio na tipografia.</span><span class="sxs-lookup"><span data-stu-id="d4d12-108">This will require a short detour into typography.</span></span> <span data-ttu-id="d4d12-109">Na tipografia, o tamanho do tipo é medido em unidades chamadas *pontos*.</span><span class="sxs-lookup"><span data-stu-id="d4d12-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="d4d12-110">Um ponto é igual a 1/72 de uma polegada.</span><span class="sxs-lookup"><span data-stu-id="d4d12-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="d4d12-111">1 pt = 1/72 polegadas</span><span class="sxs-lookup"><span data-stu-id="d4d12-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="d4d12-112">Esta é a definição do ponto de publicação de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d4d12-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="d4d12-113">Historicamente, a medida exata de um ponto variava.</span><span class="sxs-lookup"><span data-stu-id="d4d12-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="d4d12-114">Por exemplo, uma fonte de 12 pontos foi projetada para caber em uma linha de texto de 1/6 "(12/72).</span><span class="sxs-lookup"><span data-stu-id="d4d12-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="d4d12-115">Obviamente, isso não significa que cada caractere na fonte é exatamente 1/6 "de altura.</span><span class="sxs-lookup"><span data-stu-id="d4d12-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="d4d12-116">Na verdade, alguns caracteres podem ser mais altos que 1/6 ".</span><span class="sxs-lookup"><span data-stu-id="d4d12-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="d4d12-117">Por exemplo, em muitas fontes, o caractere Å é mais alto que a altura nominal da fonte.</span><span class="sxs-lookup"><span data-stu-id="d4d12-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="d4d12-118">Para exibir corretamente, a fonte precisa de algum espaço adicional entre o texto.</span><span class="sxs-lookup"><span data-stu-id="d4d12-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="d4d12-119">Esse espaço é chamado de *entrelinha*.</span><span class="sxs-lookup"><span data-stu-id="d4d12-119">This space is called the *leading*.</span></span>

<span data-ttu-id="d4d12-120">A ilustração a seguir mostra uma fonte de ponto de 72.</span><span class="sxs-lookup"><span data-stu-id="d4d12-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="d4d12-121">As linhas sólidas mostram uma "delimitadora de altura 1" em volta do texto.</span><span class="sxs-lookup"><span data-stu-id="d4d12-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="d4d12-122">A linha tracejada é chamada de *linha de base*.</span><span class="sxs-lookup"><span data-stu-id="d4d12-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="d4d12-123">A maioria dos caracteres em uma fonte é REST na linha de base.</span><span class="sxs-lookup"><span data-stu-id="d4d12-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="d4d12-124">A altura da fonte inclui a parte acima da linha de base (a *ascendente*) e a parte abaixo da linha de base (o *descendente*).</span><span class="sxs-lookup"><span data-stu-id="d4d12-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="d4d12-125">Na fonte mostrada aqui, o ascendente é de 56 pontos e o descendente é de 16 pontos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![uma ilustração que mostra uma fonte de ponto de 72.](images/graphics11.png)

<span data-ttu-id="d4d12-127">No entanto, quando se trata de uma exibição de computador, a medição do tamanho do texto é problemática, pois os pixels não têm o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="d4d12-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="d4d12-128">O tamanho de um pixel depende de dois fatores: a resolução de vídeo e o tamanho físico do monitor.</span><span class="sxs-lookup"><span data-stu-id="d4d12-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="d4d12-129">Portanto, as polegadas físicas não são uma medida útil, pois não há nenhuma relação fixa entre polegadas físicas e pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="d4d12-130">Em vez disso, as fontes são medidas em unidades *lógicas* .</span><span class="sxs-lookup"><span data-stu-id="d4d12-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="d4d12-131">Uma fonte de ponto 72 é definida para ter uma polegada lógica de altura.</span><span class="sxs-lookup"><span data-stu-id="d4d12-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="d4d12-132">Em seguida, as polegadas lógicas são convertidas em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="d4d12-133">Por muitos anos, o Windows usou a seguinte conversão: uma polegada lógica é igual a 96 pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="d4d12-134">Usando esse fator de dimensionamento, uma fonte de ponto de 72 é renderizada como 96 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="d4d12-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="d4d12-135">Uma fonte de 12 pontos tem 16 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="d4d12-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="d4d12-136">12 pontos = 12/72 polegada lógica = 1/6 de polegada lógica = 96/6 pixels = 16 pixels</span><span class="sxs-lookup"><span data-stu-id="d4d12-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="d4d12-137">Esse fator de dimensionamento é descrito como 96 pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="d4d12-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="d4d12-138">Os pontos de termo derivam da impressão, em que pontos físicos de tinta são colocados em papel.</span><span class="sxs-lookup"><span data-stu-id="d4d12-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="d4d12-139">Para o computador ser exibido, seria mais preciso dizer 96 pixels por polegada lógica, mas o termo DPI travou.</span><span class="sxs-lookup"><span data-stu-id="d4d12-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="d4d12-140">Como os tamanhos de pixel reais variam, o texto legível em um monitor pode ser muito pequeno em outro monitor.</span><span class="sxs-lookup"><span data-stu-id="d4d12-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="d4d12-141">Além disso, as pessoas têm preferências diferentes — algumas pessoas preferem texto maior.</span><span class="sxs-lookup"><span data-stu-id="d4d12-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="d4d12-142">Por esse motivo, o Windows permite que o usuário altere a configuração de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="d4d12-143">Por exemplo, se o usuário definir a exibição como 144 DPI, uma fonte de ponto 72 será de 144 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="d4d12-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="d4d12-144">As configurações de DPI padrão são 100% (96 DPI), 125% (120 DPI) e 150% (144 DPI).</span><span class="sxs-lookup"><span data-stu-id="d4d12-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="d4d12-145">O usuário também pode aplicar uma configuração personalizada.</span><span class="sxs-lookup"><span data-stu-id="d4d12-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="d4d12-146">A partir do Windows 7, o DPI é uma configuração por usuário.</span><span class="sxs-lookup"><span data-stu-id="d4d12-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="d4d12-147">Dimensionamento do DWM</span><span class="sxs-lookup"><span data-stu-id="d4d12-147">DWM Scaling</span></span>

<span data-ttu-id="d4d12-148">Se um programa não considerar DPI, os seguintes defeitos podem ser aparentes em configurações de alto DPI:</span><span class="sxs-lookup"><span data-stu-id="d4d12-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="d4d12-149">Elementos de interface do usuário recortados.</span><span class="sxs-lookup"><span data-stu-id="d4d12-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="d4d12-150">Layout incorreto.</span><span class="sxs-lookup"><span data-stu-id="d4d12-150">Incorrect layout.</span></span>
-   <span data-ttu-id="d4d12-151">Bitmaps e ícones pixelado.</span><span class="sxs-lookup"><span data-stu-id="d4d12-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="d4d12-152">Coordenadas incorretas do mouse, que podem afetar os testes de clique, arrastar e soltar e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d4d12-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="d4d12-153">Para garantir que os programas mais antigos funcionem em configurações de alto DPI, o DWM implementa um fallback útil.</span><span class="sxs-lookup"><span data-stu-id="d4d12-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="d4d12-154">Se um programa não estiver marcado como tendo reconhecimento de DPI, o DWM dimensionará toda a interface do usuário para corresponder à configuração de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="d4d12-155">Por exemplo, às 144 DPI, a interface do usuário é dimensionada por 150%, incluindo texto, elementos gráficos, controles e tamanhos de janelas.</span><span class="sxs-lookup"><span data-stu-id="d4d12-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="d4d12-156">Se o programa criar uma janela 500 × 500, a janela aparecerá na verdade como 750 × 750 pixels e o conteúdo da janela será dimensionado de acordo.</span><span class="sxs-lookup"><span data-stu-id="d4d12-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="d4d12-157">Esse comportamento significa que os programas mais antigos "simplesmente funcionam" em configurações de alto DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="d4d12-158">No entanto, o dimensionamento também resulta em uma aparência um pouco borrada, pois o dimensionamento é aplicado depois que a janela é desenhada.</span><span class="sxs-lookup"><span data-stu-id="d4d12-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="d4d12-159">DPI-Aware aplicativos</span><span class="sxs-lookup"><span data-stu-id="d4d12-159">DPI-Aware Applications</span></span>

<span data-ttu-id="d4d12-160">Para evitar o dimensionamento do DWM, um programa pode se marcar como com reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="d4d12-161">Isso diz ao DWM para não executar nenhum dimensionamento automático de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="d4d12-162">Todos os novos aplicativos devem ser criados para reconhecer DPI, pois o reconhecimento de DPI melhora a aparência da interface do usuário em configurações de DPI mais altas.</span><span class="sxs-lookup"><span data-stu-id="d4d12-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="d4d12-163">Um programa declara a si mesmo o reconhecimento de DPI por meio de seu manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4d12-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="d4d12-164">Um *manifesto* é simplesmente um arquivo XML que descreve uma DLL ou um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4d12-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="d4d12-165">O manifesto normalmente é inserido no arquivo executável, embora possa ser fornecido como um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="d4d12-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="d4d12-166">Um manifesto contém informações como dependências de DLL, o nível de privilégio solicitado e a qual versão do Windows o programa foi projetado.</span><span class="sxs-lookup"><span data-stu-id="d4d12-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="d4d12-167">Para declarar que o seu programa tem reconhecimento de DPI, inclua as seguintes informações no manifesto.</span><span class="sxs-lookup"><span data-stu-id="d4d12-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="d4d12-168">A listagem mostrada aqui é apenas um manifesto parcial, mas o vinculador do Visual Studio gera o restante do manifesto para você automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d4d12-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="d4d12-169">Para incluir um manifesto parcial em seu projeto, execute as etapas a seguir no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d4d12-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="d4d12-170">No menu **projeto** , clique em **Propriedade**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="d4d12-171">No painel esquerdo, expanda **Propriedades de configuração**, expanda **ferramenta de manifesto** e clique em **entrada e saída**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="d4d12-172">Na caixa de texto **arquivos de manifesto adicionais** , digite o nome do arquivo de manifesto e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="d4d12-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="d4d12-173">Ao marcar seu programa como reconhecimento de DPI, você está dizendo ao DWM para não dimensionar a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d4d12-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="d4d12-174">Agora, se você criar uma janela 500 × 500, a janela ocupará 500 × 500 pixels, independentemente da configuração de DPI do usuário.</span><span class="sxs-lookup"><span data-stu-id="d4d12-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="d4d12-175">GDI e DPI</span><span class="sxs-lookup"><span data-stu-id="d4d12-175">GDI and DPI</span></span>

<span data-ttu-id="d4d12-176">O desenho GDI é medido em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="d4d12-177">Isso significa que se o seu programa estiver marcado como reconhecimento de DPI e você solicitar que a GDI desenhe um retângulo de 200 × 100, o retângulo resultante terá 200 pixels de largura e 100 pixels de altura na tela.</span><span class="sxs-lookup"><span data-stu-id="d4d12-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="d4d12-178">No entanto, os tamanhos de fonte GDI são dimensionados para a configuração de DPI atual.</span><span class="sxs-lookup"><span data-stu-id="d4d12-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="d4d12-179">Em outras palavras, se você criar uma fonte de ponto 72, o tamanho da fonte será 96 pixels em 96 DPI, mas 144 pixels em 144 DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="d4d12-180">Aqui está uma fonte de 72 pontos renderizada em 144 DPI usando GDI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![um diagrama que mostra o dimensionamento da fonte de DPI em GDI.](images/graphics12.png)

<span data-ttu-id="d4d12-182">Se seu aplicativo reconhece DPI e você usa GDI para desenhar, dimensione todas as suas coordenadas de desenho para corresponder ao DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="d4d12-183">Direct2D e DPI</span><span class="sxs-lookup"><span data-stu-id="d4d12-183">Direct2D and DPI</span></span>

<span data-ttu-id="d4d12-184">O Direct2D executa automaticamente o dimensionamento para corresponder à configuração de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="d4d12-185">No Direct2D, as coordenadas são medidas em unidades chamadas de DIPs ( *pixels independentes de dispositivo* ).</span><span class="sxs-lookup"><span data-stu-id="d4d12-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="d4d12-186">Um DIP é definido como 1/1/96 de uma polegada *lógica* .</span><span class="sxs-lookup"><span data-stu-id="d4d12-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="d4d12-187">No Direct2D, todas as operações de desenho são especificadas em DIPs e, em seguida, dimensionadas para a configuração de DPI atual.</span><span class="sxs-lookup"><span data-stu-id="d4d12-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="d4d12-188">Configuração de DPI</span><span class="sxs-lookup"><span data-stu-id="d4d12-188">DPI setting</span></span> | <span data-ttu-id="d4d12-189">Tamanho do DIP</span><span class="sxs-lookup"><span data-stu-id="d4d12-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="d4d12-190">96</span><span class="sxs-lookup"><span data-stu-id="d4d12-190">96</span></span>          | <span data-ttu-id="d4d12-191">1 pixel</span><span class="sxs-lookup"><span data-stu-id="d4d12-191">1 pixel</span></span>     |
| <span data-ttu-id="d4d12-192">120</span><span class="sxs-lookup"><span data-stu-id="d4d12-192">120</span></span>         | <span data-ttu-id="d4d12-193">1,25 pixels</span><span class="sxs-lookup"><span data-stu-id="d4d12-193">1.25 pixels</span></span> |
| <span data-ttu-id="d4d12-194">144</span><span class="sxs-lookup"><span data-stu-id="d4d12-194">144</span></span>         | <span data-ttu-id="d4d12-195">1,5 pixels</span><span class="sxs-lookup"><span data-stu-id="d4d12-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="d4d12-196">Por exemplo, se a configuração de DPI do usuário for 144 DPI e você solicitar que Direct2D desenhe um retângulo 200 × 100, o retângulo será de 300 × 150 pixels físicos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="d4d12-197">Além disso, DirectWrite mede os tamanhos de fonte em DIPs, em vez de pontos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="d4d12-198">Para criar uma fonte de 12 pontos, especifique 16 DIPs (12 pontos = 1/6 polegada lógica = 96/6 DIPs).</span><span class="sxs-lookup"><span data-stu-id="d4d12-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="d4d12-199">Quando o texto é desenhado na tela, Direct2D converte o DIPs em pixels físicos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="d4d12-200">O benefício desse sistema é que as unidades de medida são consistentes para o texto e o desenho, independentemente da configuração de DPI atual.</span><span class="sxs-lookup"><span data-stu-id="d4d12-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="d4d12-201">Uma palavra de cuidado: as coordenadas do mouse e da janela ainda são dadas em pixels físicos, não DIPs.</span><span class="sxs-lookup"><span data-stu-id="d4d12-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="d4d12-202">Por exemplo, se você processar a mensagem do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , a posição do mouse para baixo será fornecida em pixels físicos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="d4d12-203">Para desenhar um ponto nessa posição, você deve converter as coordenadas de pixel em DIPs.</span><span class="sxs-lookup"><span data-stu-id="d4d12-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="d4d12-204">Convertendo pixels físicos em DIPs</span><span class="sxs-lookup"><span data-stu-id="d4d12-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="d4d12-205">A conversão de pixels físicos para DIPs usa a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4d12-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="d4d12-206">DIPs = pixels/(DPI/96.0)</span><span class="sxs-lookup"><span data-stu-id="d4d12-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="d4d12-207">Para obter a configuração de DPI, chame o método [**ID2D1Factory:: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="d4d12-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="d4d12-208">O DPI é retornado como dois valores de ponto flutuante, um para o eixo x e outro para o eixo y.</span><span class="sxs-lookup"><span data-stu-id="d4d12-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="d4d12-209">Teoricamente, esses valores podem diferir.</span><span class="sxs-lookup"><span data-stu-id="d4d12-209">In theory, these values can differ.</span></span> <span data-ttu-id="d4d12-210">Calcule um fator de dimensionamento separado para cada eixo.</span><span class="sxs-lookup"><span data-stu-id="d4d12-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="d4d12-211">Aqui está uma maneira alternativa de obter a configuração de DPI se você não estiver usando Direct2D:</span><span class="sxs-lookup"><span data-stu-id="d4d12-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="d4d12-212">No Windows 10, a versão 1903,  [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) foi preterida e a recomendação é [**DisplayInformation:: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) para aplicativos da Windows Store ou [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) para aplicativos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d4d12-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="d4d12-213">Se você ainda quiser usá-lo, suprime a mensagem de erro do compilador escrevendo a linha [**#pragma Aviso (suprimir: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) logo antes da chamada [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="d4d12-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="d4d12-214">Embora não seja recomendado, é possível definir o reconhecimento de DPI padrão programaticamente usando [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span><span class="sxs-lookup"><span data-stu-id="d4d12-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="d4d12-215">Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para a alteração do modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="d4d12-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="d4d12-216">Se você estiver configurando o modo de reconhecimento de DPI de processo padrão programaticamente, deverá chamar a API correspondente antes que quaisquer HWNDs tenham sido criados.</span><span class="sxs-lookup"><span data-stu-id="d4d12-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="d4d12-217">Para obter informações, consulte [definindo o reconhecimento de DPI padrão para um processo](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="d4d12-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="d4d12-218">Redimensionando o destino de renderização</span><span class="sxs-lookup"><span data-stu-id="d4d12-218">Resizing the Render Target</span></span>

<span data-ttu-id="d4d12-219">Se o tamanho da janela for alterado, você deverá redimensionar o destino de renderização para corresponder.</span><span class="sxs-lookup"><span data-stu-id="d4d12-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="d4d12-220">Na maioria dos casos, também será necessário atualizar o layout e redesenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="d4d12-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="d4d12-221">O código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="d4d12-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="d4d12-222">A função [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) Obtém o novo tamanho da área do cliente, em pixels físicos (não DIPs).</span><span class="sxs-lookup"><span data-stu-id="d4d12-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="d4d12-223">O método [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) atualiza o tamanho do destino de renderização, também especificado em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="d4d12-224">A função [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) força um redesenho adicionando toda a área do cliente à região de atualização da janela.</span><span class="sxs-lookup"><span data-stu-id="d4d12-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="d4d12-225">(Consulte [pintando a janela](painting-the-window.md), no módulo 1.)</span><span class="sxs-lookup"><span data-stu-id="d4d12-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="d4d12-226">À medida que a janela aumenta ou diminui, normalmente, você precisará recalcular a posição dos objetos desenhados.</span><span class="sxs-lookup"><span data-stu-id="d4d12-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="d4d12-227">Por exemplo, no programa de círculo, o raio e o ponto central devem ser atualizados:</span><span class="sxs-lookup"><span data-stu-id="d4d12-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="d4d12-228">O método [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) retorna o tamanho do destino de renderização em DIPs (não pixels), que é a unidade apropriada para calcular o layout.</span><span class="sxs-lookup"><span data-stu-id="d4d12-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="d4d12-229">Há um método fortemente relacionado, [**ID2D1RenderTarget:: Getpixelize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), que retorna o tamanho em pixels físicos.</span><span class="sxs-lookup"><span data-stu-id="d4d12-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="d4d12-230">Para um destino de renderização **HWND** , esse valor corresponde ao tamanho retornado por [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span><span class="sxs-lookup"><span data-stu-id="d4d12-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="d4d12-231">Mas lembre-se de que o desenho é executado em DIPs, e não em pixels.</span><span class="sxs-lookup"><span data-stu-id="d4d12-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="d4d12-232">Avançar</span><span class="sxs-lookup"><span data-stu-id="d4d12-232">Next</span></span>

[<span data-ttu-id="d4d12-233">Usando a cor em Direct2D</span><span class="sxs-lookup"><span data-stu-id="d4d12-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
