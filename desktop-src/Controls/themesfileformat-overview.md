---
title: Formato de arquivo de tema
description: Este documento discute o formato dos arquivos de tema (. Theme). Um arquivo. Theme é um arquivo de texto. ini que é dividido em seções, que especificam elementos visuais que aparecem em uma área de trabalho do Windows. Os nomes de seção são encapsulados entre colchetes (\ \) no arquivo. ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/16/2020
ms.locfileid: "103824047"
---
# <a name="theme-file-format"></a><span data-ttu-id="4ea5e-105">Formato de arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-105">Theme File Format</span></span>

<span data-ttu-id="4ea5e-106">Este documento discute o formato dos arquivos de tema (. Theme).</span><span class="sxs-lookup"><span data-stu-id="4ea5e-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="4ea5e-107">Um arquivo. Theme é um arquivo de texto. ini que é dividido em seções, que especificam elementos visuais que aparecem em uma área de trabalho do Windows.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="4ea5e-108">Os nomes de seção são encapsulados entre colchetes ( \[ \] ) no arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="4ea5e-109">Um novo formato de arquivo,. themepack, foi introduzido com o Windows 7 para ajudar os usuários a compartilhar temas.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="4ea5e-110">Os temas podem ser selecionados no painel de controle de personalização somente no Windows 7 Home Premium ou superior, ou somente no Windows Server 2008 R2 quando o componente da área de trabalho é instalado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="4ea5e-111">Os tópicos a seguir são discutidos neste artigo.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="4ea5e-112">Criando um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="4ea5e-113">Descrição de um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="4ea5e-114">[\[Seção de tema \]](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="4ea5e-115">[\[Seção cores do painel de controle \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="4ea5e-116">[\[\\Seção cursores do painel de controle \]](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="4ea5e-117">[\[\\Seção área de trabalho do painel de controle \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="4ea5e-118">[\[Seção de apresentação de slides \]](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="4ea5e-119">[\[Seção de métricas \]](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="4ea5e-120">[\[Seção de estilos visuais \]](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="4ea5e-121">[\[AppEvents de sons \] e \[ \] seções (sons)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="4ea5e-122">[\[Seção de inicialização \]](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="4ea5e-123">[\[\]Seção MasterThemeSelector](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="4ea5e-124">Exemplo de um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="4ea5e-125">Instalando arquivos de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="4ea5e-126">Pacotes de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="4ea5e-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ea5e-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="4ea5e-128">Criando um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-128">Creating a Theme File</span></span>

<span data-ttu-id="4ea5e-129">Um arquivo. Theme permite que você altere a aparência de determinados elementos da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="4ea5e-130">Você pode criar ou modificar um arquivo. Theme de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="4ea5e-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="4ea5e-131">Modifique as configurações de personalização ou exibição no painel de controle e salve as configurações como um arquivo. Theme.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="4ea5e-132">Consulte a ajuda do Windows para obter instruções.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="4ea5e-133">Crie um arquivo. Theme manualmente para um nível maior de controle sobre os detalhes do seu tema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="4ea5e-134">Para disponibilizar seu tema para outros usuários, você deve fornecer o arquivo. theme, bem como a imagem de plano de fundo, a proteção de tela e os arquivos de ícones.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="4ea5e-135">Você pode fazer isso com um [pacote de temas](#theme-packs).</span><span class="sxs-lookup"><span data-stu-id="4ea5e-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="4ea5e-136">Descrição de um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-136">Description of a Theme File</span></span>

<span data-ttu-id="4ea5e-137">Os arquivos de tema têm várias seções obrigatórias e opcionais.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="4ea5e-138">O exemplo a seguir descreve as seções de arquivos. Theme e fornece exemplos de como especificar alterações para os diferentes elementos.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="4ea5e-139">\[Seção de tema \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-140">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-140">This section is optional.</span></span> <span data-ttu-id="4ea5e-141">Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="4ea5e-142">A \[ \] seção tema identifica o nome do seu tema personalizado e especifica o logotipo da marca do tema e os ícones da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="4ea5e-143">A primeira parte da \[ seção Theme \] contém os dois elementos a seguir:</span><span class="sxs-lookup"><span data-stu-id="4ea5e-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="4ea5e-144">Elemento</span><span class="sxs-lookup"><span data-stu-id="4ea5e-144">Element</span></span>                                                                                                                    | <span data-ttu-id="4ea5e-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ea5e-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea5e-146">DisplayName = nome</span><span class="sxs-lookup"><span data-stu-id="4ea5e-146">DisplayName=name</span></span><br/> <span data-ttu-id="4ea5e-147">ou</span><span class="sxs-lookup"><span data-stu-id="4ea5e-147">or</span></span><br/> <span data-ttu-id="4ea5e-148">DisplayName = @module ,-stringid</span><span class="sxs-lookup"><span data-stu-id="4ea5e-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="4ea5e-149">exemplo: DisplayName = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="4ea5e-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="4ea5e-150">DisplayName é o nome do tema que aparecerá no painel de controle de personalização.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="4ea5e-151">Pode ser uma cadeia de caracteres ou uma referência a um nome localizado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="4ea5e-152">Esse campo é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-152">This field is optional.</span></span> <span data-ttu-id="4ea5e-153">Se ele estiver ausente, o nome de arquivo do tema será usado como tema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="4ea5e-154">BrandImage = caminho para a imagem</span><span class="sxs-lookup"><span data-stu-id="4ea5e-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="4ea5e-155">exemplo: BrandImage = c: \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="4ea5e-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="4ea5e-156">**Windows 7 e posterior** BrandImage especifica o caminho para um arquivo gráfico com marca que é incorporado na visualização do tema no painel de controle de personalização.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="4ea5e-157">O ícone gráfico deve ser um arquivo PNG.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="4ea5e-158">O gráfico é dimensionado para 80x240 pixels, portanto, é recomendável que você forneça uma imagem desse tamanho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="4ea5e-159">A Galeria de temas respeita as regiões transparentes de seu ícone de marca.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="4ea5e-160">Esse campo é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-160">This field is optional.</span></span> <span data-ttu-id="4ea5e-161">Se estiver ausente, nenhum logotipo será exibido como o ícone de tema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="4ea5e-162">O restante da \[ seção tema \] especifica ícones personalizados para recursos de área de trabalho, como computador, meus documentos, rede e lixeira.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="4ea5e-163">Se você não especificar ícones personalizados da área de trabalho, a área de trabalho exibirá os ícones padrão da área de trabalho do sistema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="4ea5e-164">Veja a seguir dois exemplos de como um arquivo. Theme define o ícone do **computador** .</span><span class="sxs-lookup"><span data-stu-id="4ea5e-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="4ea5e-165">Estes são os valores para os ícones de área de trabalho padrão no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-165">The following are values for the default desktop icons in Windows 7.</span></span>


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a><span data-ttu-id="4ea5e-166">\[Seção cores do painel de controle \\ \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-167">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-167">This section is optional.</span></span> <span data-ttu-id="4ea5e-168">Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="4ea5e-169">Se seu tema usa o estilo visual Aero, você deve evitar substituir os valores padrão nesta seção.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="4ea5e-170">A cor dos elementos, como barras de rolagem, texto e botões, é personalizável.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="4ea5e-171">O arquivo. Theme especifica os valores RGB a serem alterados para esses elementos.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="4ea5e-172">Os valores substituem os valores padrão do estilo visual e são usados quando seu tema se baseia nos temas Windows clássico, Windows 7 Basic ou Alto Contraste.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="4ea5e-173">Veja a seguir um exemplo de como as cores são definidas.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-173">Following is an example of how colors are set.</span></span>


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a><span data-ttu-id="4ea5e-174">\[\\Seção cursores do painel de controle \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-175">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-175">This section is optional.</span></span> <span data-ttu-id="4ea5e-176">Se você não incluir esta seção no arquivo. theme, o sistema usará cursores padrão.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="4ea5e-177">Um tema também pode alterar a aparência dos cursores.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="4ea5e-178">Para fazer isso, você cria arquivos. cur para substituir os cursores padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="4ea5e-179">O exemplo a seguir é de um arquivo. Theme que define os cursores de um tema chamado *esportes*.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a><span data-ttu-id="4ea5e-180">\[\\Seção área de trabalho do painel de controle \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-181">Esta seção é necessária.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-181">This section is required.</span></span> <span data-ttu-id="4ea5e-182">Se você não incluir esta seção no arquivo. theme, o sistema ignorará o tema e não exibirá o tema no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="4ea5e-183">Você pode criar um plano de fundo personalizado da área de trabalho e especificar um caminho para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="4ea5e-184">O exemplo a seguir mostra como modificar a aparência da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-184">The following example shows how to modify the desktop appearance.</span></span>


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a><span data-ttu-id="4ea5e-185">\[Seção de apresentação de slides \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="4ea5e-186">**Windows 7 e posterior.**</span><span class="sxs-lookup"><span data-stu-id="4ea5e-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-187">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-187">This section is optional.</span></span> <span data-ttu-id="4ea5e-188">Se você não incluir esta seção no arquivo. theme, o sistema usará a imagem de plano de fundo da área de trabalho especificada na \[ seção área de trabalho do painel de controle \\ \] .</span><span class="sxs-lookup"><span data-stu-id="4ea5e-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="4ea5e-189">Se você incluir esta seção, deverá especificar as configurações de apresentação de slides aqui.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="4ea5e-190">O plano de fundo de seu tema pode ser uma apresentação de slides de imagens armazenadas localmente ou de imagens servidas por um RSS feed.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="4ea5e-191">A \[ \] seção de apresentação de slides do arquivo contém os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="4ea5e-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ea5e-192">Atributo</span><span class="sxs-lookup"><span data-stu-id="4ea5e-192">Attribute</span></span></th>
<th><span data-ttu-id="4ea5e-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ea5e-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ea5e-194">Intervalo = número de milissegundos</span><span class="sxs-lookup"><span data-stu-id="4ea5e-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="4ea5e-195">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-195">Required.</span></span> <span data-ttu-id="4ea5e-196">Interval é um número que determina com que frequência o plano de fundo é alterado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="4ea5e-197">É medido em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea5e-198">Ordem aleatória = 0 ou 1</span><span class="sxs-lookup"><span data-stu-id="4ea5e-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="4ea5e-199">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-199">Required.</span></span> <span data-ttu-id="4ea5e-200">Ordem aleatória identifica se a ordem aleatória do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="4ea5e-201">0 = Desabilitado</span><span class="sxs-lookup"><span data-stu-id="4ea5e-201">0 = Disabled</span></span><br/> <span data-ttu-id="4ea5e-202">1 = Habilitado</span><span class="sxs-lookup"><span data-stu-id="4ea5e-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea5e-203">RSSFeed = URL para RSS feed</span><span class="sxs-lookup"><span data-stu-id="4ea5e-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="4ea5e-204">Obrigatório se ImagesRootPath não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="4ea5e-205">RSSFeed especifica um RSS feed a ser usado como a apresentação de slides em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="4ea5e-206">Para que o feed funcione, você precisa fazer referência a imagens de alta resolução que aderem ao &quot; padrão de compartimentos &quot; usado pela <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plataforma Windows RSS</a>.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="4ea5e-207">Devido a essa limitação, os arquivos. Theme que incluem um RSS feed devem ser criados manualmente.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea5e-208">Você não pode especificar um RSSFeed e um ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ea5e-209">ImagesRootPath = caminho para a pasta de imagem</span><span class="sxs-lookup"><span data-stu-id="4ea5e-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="4ea5e-210">Obrigatório se RSSFeed não for especificado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="4ea5e-211">ImagesRootPath especifica um caminho para um conjunto de imagens que você deseja usar como a apresentação de slides em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="4ea5e-212">As imagens nas subpastas não são incluídas na apresentação de slides.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="4ea5e-213">ImagesRootPath dá suporte a substituições de variável de ambiente no caminho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ea5e-214">Você não pode especificar um RSSFeed e um ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ea5e-215">Item<em>N</em>caminho = caminho (s) para imagem (ns) específica (s)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="4ea5e-216">Para uso com ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="4ea5e-217">O item<em>N</em>caminho Especifica caminhos para imagens específicas, para que você possa limitar a apresentação de slides a imagens específicas, em vez de todas as imagens em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="4ea5e-218">Se nenhum caminho for especificado, todas as imagens no caminho ImagesRootPath serão usadas na apresentação de slides, incluindo as imagens adicionadas após a criação e instalação do tema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="4ea5e-219">O caminho<em>N</em>do item dá suporte às substituições de variável de ambiente no caminho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="4ea5e-220"><em>N</em> é 0, 1, 2 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4ea5e-221">Os exemplos a seguir mostram como um arquivo. Theme especifica a apresentação de slides para incluir um conjunto de imagens armazenadas localmente.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



<span data-ttu-id="4ea5e-222">O exemplo a seguir é um modelo para um arquivo. Theme que cria uma apresentação de slides de plano de fundo da área de trabalho usando imagens de um RSS feed.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="4ea5e-223">Siga estas etapas para personalizar o modelo:</span><span class="sxs-lookup"><span data-stu-id="4ea5e-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="4ea5e-224">Copie o exemplo a seguir e cole-o em um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="4ea5e-225">Substitua {ThemeName} pelo nome que você deseja exibir na Galeria de temas do painel de controle de personalização.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="4ea5e-226">Substitua {rssfeedurl} pelo caminho completo para um RSS feed compatível.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="4ea5e-227">Salve as alterações como um arquivo com a extensão ". Theme".</span><span class="sxs-lookup"><span data-stu-id="4ea5e-227">Save the changes as a file with the ".theme" extension.</span></span>


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a><span data-ttu-id="4ea5e-228">\[Seção de métricas \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-229">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-229">This section is optional.</span></span> <span data-ttu-id="4ea5e-230">Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações de estilo visual padrão.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="4ea5e-231">Você pode especificar as métricas do sistema em um arquivo. Theme.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="4ea5e-232">As métricas do sistema são as dimensões de vários elementos de exibição, como a largura da borda da janela, a altura do ícone ou a largura da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="4ea5e-233">Os valores NonclientMetrics e IconMetrics são estruturas binárias definidas por NONCLIENTMETRICS e ICONMETRICS em winuser. h.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="4ea5e-234">A seguir, um exemplo de como alterar as métricas do sistema.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-234">Following is an example of how to change system metrics.</span></span>


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a><span data-ttu-id="4ea5e-235">\[Seção de estilos visuais \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-236">Esta seção é necessária.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-236">This section is required.</span></span> <span data-ttu-id="4ea5e-237">Se você não incluir esta seção no arquivo. theme, o sistema ignorará o tema e não exibirá o tema no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="4ea5e-238">Você pode fornecer informações específicas sobre o tamanho e a cor dos elementos da área de trabalho nos arquivos. msstyles.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="4ea5e-239">As seções de cor e tamanho dos arquivos. Theme podem ser substituídas por arquivos. msstyles que permitem que você modifique os elementos da área de trabalho com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="4ea5e-240">Esses arquivos são especificados na seção estilos visuais de um arquivo. Theme.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="4ea5e-241">Veja a seguir um exemplo de uma seção de estilos visuais.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="4ea5e-242">A adição de um elemento Path a um arquivo. msstyles é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="4ea5e-243">Se você fornecer um caminho, deverá remover as seções métricas e cor do arquivo. Theme.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="4ea5e-244">Quando essas seções são removidas, as cores, as fontes e os tamanhos de um tema são provenientes do arquivo. msstyles e correspondem à intenção do autor do. msstyles.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="4ea5e-245">A falha na remoção das seções métrica e cor pode fazer com que o Windows ou os aplicativos tenham problemas de desenho.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="4ea5e-246">**Windows Vista/Windows 7:** Quando o caminho aponta para Aero. msstyles, você pode especificar a cor de vidro desejada, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="4ea5e-247">**Windows 7:** Quando o caminho aponta para Aero. msstyles, você também pode especificar o valor de transparência desejado, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="4ea5e-248">Se os valores de transparência e ColorizationColor corresponderem exatamente a uma cor do sistema, o painel de controle de personalização exibirá o nome do sistema para a cor.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="4ea5e-249">Caso contrário, a cor será rotulada como "personalizado".</span><span class="sxs-lookup"><span data-stu-id="4ea5e-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="4ea5e-250">O seguinte mostra uma seção VisualStyles para o tema básico do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="4ea5e-251">O seguinte mostra uma seção VisualStyles para o tema clássico do Windows.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="4ea5e-252">O seguinte mostra uma seção VisualStyles para um tema Alto Contraste preto.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="4ea5e-253">\[AppEvents de sons \] e \[ \] seções (sons)</span><span class="sxs-lookup"><span data-stu-id="4ea5e-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-254">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-254">This section is optional.</span></span> <span data-ttu-id="4ea5e-255">Se você não incluir esta seção no arquivo. theme, o sistema usará as configurações de som padrão.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="4ea5e-256">O usuário pode selecionar o ícone de **som** no painel de controle para associar sons a eventos que ocorrem em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="4ea5e-257">Por exemplo, um arquivo. wav pode ser executado quando um aplicativo é aberto.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="4ea5e-258">Um arquivo. Theme pode especificar arquivos. wav para substituir os padrões.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="4ea5e-259">O exemplo a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-259">The following example shows how to do this.</span></span>


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



<span data-ttu-id="4ea5e-260">**Windows 7 e posterior:** Um nome de esquema de som pode ser especificado em vez de listar cada som separadamente.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="4ea5e-261">O valor de schemeName especifica o nome do esquema de som ou o nome do esquema de som localizado, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="4ea5e-262">\[Seção de inicialização \]</span><span class="sxs-lookup"><span data-stu-id="4ea5e-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-263">**As proteções de tela são preteridas na atualização de aniversário do Windows 10 e além disso.**</span><span class="sxs-lookup"><span data-stu-id="4ea5e-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="4ea5e-264">Esta seção é opcional.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-264">This section is optional.</span></span> <span data-ttu-id="4ea5e-265">Se você não incluir esta seção no arquivo. theme, nenhuma proteção de tela será usada.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="4ea5e-266">No arquivo. theme, você pode especificar a proteção de tela para o Windows usar.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="4ea5e-267">O exemplo a seguir mostra a isso.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="4ea5e-268">\[\]Seção MasterThemeSelector</span><span class="sxs-lookup"><span data-stu-id="4ea5e-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="4ea5e-269">Esta seção é necessária.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-269">This section is required.</span></span> <span data-ttu-id="4ea5e-270">Se você não incluir esta seção no arquivo. theme, o sistema ignorará o tema e não exibirá o tema no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="4ea5e-271">A seção seletor de tema mestre do arquivo. Theme deve ser sempre incluída como uma marca que indica que o arquivo é válido.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="4ea5e-272">Você não tem uma opção de valores para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="4ea5e-273">O seguinte mostra isso.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="4ea5e-274">Exemplo de um arquivo de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-274">Example of a Theme File</span></span>

<span data-ttu-id="4ea5e-275">O exemplo a seguir mostra um arquivo. Theme completo.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-275">The following example shows a complete .theme file.</span></span>


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a><span data-ttu-id="4ea5e-276">Instalando arquivos de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-276">Installing Theme Files</span></span>

<span data-ttu-id="4ea5e-277">Quando o Windows é inicializado, o sistema operacional enumera os subdiretórios de primeiro nível dos recursos de% WinDir% \\ \\ para identificar os temas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="4ea5e-278">Os arquivos de tema padrão do sistema estão localizados em temas de recursos de% WinDir% \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="4ea5e-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="4ea5e-279">Os arquivos de tema do usuário são armazenados em% windir% \\ Users \\ <username> \\ AppData \\ local \\ Microsoft \\ Windows \\ Themes.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="4ea5e-280">Um arquivo. Theme tem associações de arquivo; Portanto, os aplicativos de instalador de tema podem chamar [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) em um arquivo. Theme para abrir a janela de **personalização** no painel de controle para o tema especificado.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="4ea5e-281">Pacotes de tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-281">Theme Packs</span></span>

<span data-ttu-id="4ea5e-282">**Windows 7 e posterior.**</span><span class="sxs-lookup"><span data-stu-id="4ea5e-282">**Windows 7 and later.**</span></span> <span data-ttu-id="4ea5e-283">Um pacote de temas é um arquivo. cab que contém não apenas o arquivo. theme, mas também os arquivos necessários para implementar o tema em outro computador, como arquivos de som e imagens.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="4ea5e-284">Os usuários podem criar pacotes de tema por meio do painel de controle de personalização.</span><span class="sxs-lookup"><span data-stu-id="4ea5e-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="4ea5e-285">Os tipos de arquivo com suporte incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4ea5e-285">Supported file types include the following:</span></span>



| <span data-ttu-id="4ea5e-286">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="4ea5e-286">File type</span></span>    | <span data-ttu-id="4ea5e-287">Extensão</span><span class="sxs-lookup"><span data-stu-id="4ea5e-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="4ea5e-288">Tema</span><span class="sxs-lookup"><span data-stu-id="4ea5e-288">Theme</span></span>        | <span data-ttu-id="4ea5e-289">.theme</span><span class="sxs-lookup"><span data-stu-id="4ea5e-289">.theme</span></span>                              |
| <span data-ttu-id="4ea5e-290">Imagem</span><span class="sxs-lookup"><span data-stu-id="4ea5e-290">Image</span></span>        | <span data-ttu-id="4ea5e-291">. jpg,. jpeg,. bmp,. dib,. tif,. png</span><span class="sxs-lookup"><span data-stu-id="4ea5e-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="4ea5e-292">Som</span><span class="sxs-lookup"><span data-stu-id="4ea5e-292">Sound</span></span>        | <span data-ttu-id="4ea5e-293">.wav</span><span class="sxs-lookup"><span data-stu-id="4ea5e-293">.wav</span></span>                                |
| <span data-ttu-id="4ea5e-294">Cursor do mouse</span><span class="sxs-lookup"><span data-stu-id="4ea5e-294">Mouse cursor</span></span> | <span data-ttu-id="4ea5e-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="4ea5e-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="4ea5e-296">Ícone da área de trabalho</span><span class="sxs-lookup"><span data-stu-id="4ea5e-296">Desktop icon</span></span> | <span data-ttu-id="4ea5e-297">.ico</span><span class="sxs-lookup"><span data-stu-id="4ea5e-297">.ico</span></span>                                |
| <span data-ttu-id="4ea5e-298">Logotipo da marca</span><span class="sxs-lookup"><span data-stu-id="4ea5e-298">Brand logo</span></span>   | <span data-ttu-id="4ea5e-299">.png</span><span class="sxs-lookup"><span data-stu-id="4ea5e-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="4ea5e-300">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ea5e-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea5e-301">Visão geral dos estilos visuais</span><span class="sxs-lookup"><span data-stu-id="4ea5e-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

