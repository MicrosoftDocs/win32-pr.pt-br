---
title: Suporte a temas de Alto Contraste
description: Este tópico compara o suporte para temas de alto contraste no Windows 8 para as versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um aplicativo do Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824002"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="aa8a6-103">Suporte a temas de Alto Contraste</span><span class="sxs-lookup"><span data-stu-id="aa8a6-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="aa8a6-104">Este tópico compara o suporte para temas de alto contraste no Windows 8 para as versões anteriores do Windows e explica como dar suporte a temas de alto contraste em um aplicativo do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="aa8a6-105">Ele inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="aa8a6-106">Visão geral do suporte para temas de Alto Contraste</span><span class="sxs-lookup"><span data-stu-id="aa8a6-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="aa8a6-107">Suporte a temas de Alto Contraste no Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="aa8a6-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="aa8a6-108">Adicionando uma seção de compatibilidade ao manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="aa8a6-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="aa8a6-109">Detectando Alto Contraste em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="aa8a6-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="aa8a6-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8a6-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="aa8a6-111">Visão geral do suporte para temas de Alto Contraste</span><span class="sxs-lookup"><span data-stu-id="aa8a6-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="aa8a6-112">O Windows 7 e versões anteriores dão suporte a dois modelos de temas, incluindo o modelo clássico do Windows herdado e os estilos visuais atuais.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="aa8a6-113">O modelo clássico do Windows foi mantido pelo Windows 7 principalmente para dar suporte a vários temas de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="aa8a6-114">No entanto, o modelo clássico do Windows tem uma série de desvantagens:</span><span class="sxs-lookup"><span data-stu-id="aa8a6-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="aa8a6-115">Não há suporte para temas que usam estilos visuais, como o Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="aa8a6-116">Os usuários de temas de alto contraste devem usar a interface do usuário clássica do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="aa8a6-117">Não há suporte para recursos de interface do usuário que dependem de Gerenciador de Janelas da Área de Trabalho (DWM) para execução, como visualizações de miniatura e a lupa de tela cheia que foi introduzida no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="aa8a6-118">Os desenvolvedores devem manter dois caminhos de código separados para dar suporte aos dois modelos de temas diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="aa8a6-119">No Windows 8 e posterior, as seguintes alterações no modelo de temas abordam as desvantagens anteriores:</span><span class="sxs-lookup"><span data-stu-id="aa8a6-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="aa8a6-120">O modelo de tema clássico do Windows não tem mais suporte, permitindo que os desenvolvedores mantenham apenas um caminho de código para aplicativos direcionados apenas para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="aa8a6-121">Como os estilos visuais e o DWM estão no Windows 8, os usuários de alto contraste têm acesso a recursos como visualizações de miniatura e a lupa de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="aa8a6-122">Os estilos visuais dão suporte à definição das cores de vários elementos da interface do usuário, permitindo que usuários de alto contraste personalizem a interface do usuário para acomodar necessidades e preferências individuais.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="aa8a6-123">O Windows 8 inclui suporte de compatibilidade para aplicativos existentes que são projetados para usar temas de alto contraste com base no modelo clássico do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="aa8a6-124">Suporte a temas de Alto Contraste no Windows 8 e posterior</span><span class="sxs-lookup"><span data-stu-id="aa8a6-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="aa8a6-125">No Windows 8, como os estilos visuais estão no modo de alto contraste, o suporte a temas de alto contraste é muito simples, desde que você preste atenção às diretrizes a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="aa8a6-126">Tamanhos de fonte e de controle.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-126">Font and control sizes.</span></span> <span data-ttu-id="aa8a6-127">Para garantir que sua interface do usuário seja acessível a usuários com deficiências, defina tamanhos de fonte de acordo com as configurações de tema atuais.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="aa8a6-128">Defina o tamanho dos controles como, pelo menos, o tamanho padrão.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="aa8a6-129">Cores.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-129">Colors.</span></span> <span data-ttu-id="aa8a6-130">Evite usar cores embutidas em código.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="aa8a6-131">Em vez disso, use as cores do sistema porque elas se baseiam no tema atual.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="aa8a6-132">O uso de cores personalizadas pode interferir e substituir as cores nos temas de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="aa8a6-133">Manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-133">Application manifest.</span></span> <span data-ttu-id="aa8a6-134">Os aplicativos projetados para trabalhar com os novos temas de alto contraste devem ter uma seção de compatibilidade de aplicativos definida em seu manifesto que contenha os GUIDs de compatibilidade do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="aa8a6-135">Caso contrário, o Windows pressupõe que o aplicativo foi projetado para uma versão mais antiga do Windows e renderiza a interface do usuário do aplicativo simulando o modelo clássico de tema do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="aa8a6-136">Adicionando uma seção de compatibilidade ao manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="aa8a6-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="aa8a6-137">Um manifesto de aplicativo é um arquivo XML que descreve os requisitos de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="aa8a6-138">A seção de compatibilidade do manifesto identifica as versões do Windows com suporte no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="aa8a6-139">Os GUIDs a seguir são usados na seção de compatibilidade para identificar as várias versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="aa8a6-140">Versão</span><span class="sxs-lookup"><span data-stu-id="aa8a6-140">Version</span></span>       | <span data-ttu-id="aa8a6-141">GUID</span><span class="sxs-lookup"><span data-stu-id="aa8a6-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="aa8a6-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa8a6-142">Windows Vista</span></span> | <span data-ttu-id="aa8a6-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="aa8a6-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="aa8a6-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa8a6-144">Windows 7</span></span>     | <span data-ttu-id="aa8a6-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="aa8a6-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="aa8a6-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa8a6-146">Windows 8</span></span>     | <span data-ttu-id="aa8a6-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="aa8a6-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="aa8a6-148">A seção de compatibilidade pode especificar várias versões do Windows, mas cada uma delas deve estar contida em sua própria `<supportedOS/>` marca.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="aa8a6-149">O exemplo a seguir mostra um manifesto do aplicativo que especifica o Windows 7 e o Windows 8 na seção de compatibilidade:</span><span class="sxs-lookup"><span data-stu-id="aa8a6-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="aa8a6-150">Se um aplicativo não tiver um manifesto de compatibilidade, ele será considerado um aplicativo do Windows Vista e não usará controles com temas na área do cliente quando um tema de alto contraste estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="aa8a6-151">Além disso, o comportamento de algumas funções de estilos visuais é afetado.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="aa8a6-152">Por exemplo, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) retornam false, enquanto [**OPENTHEMEDATA**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) retornam um identificador nulo.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="aa8a6-153">Isso é para o suporte à compatibilidade, de modo que os aplicativos criados antes do Windows 8 ainda possam renderizar sua interface do usuário da mesma forma que o modo de alto contraste das versões anteriores do Windows em que os estilos visuais não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="aa8a6-154">No Windows 8, o aplicativo ainda recebe os benefícios da composição da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="aa8a6-155">Isso significa, por exemplo, que aplicativos de usabilidade, como a lupa de tela inteira, não dependem do status de um manifesto de aplicativo individual.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="aa8a6-156">O aplicativo de usabilidade continua funcionando no modo de alto contraste com um aplicativo que não se identifica como compatível com o Windows 8 em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="aa8a6-157">As imagens a seguir mostram uma caixa de diálogo simples em alto contraste no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![caixa de diálogo hig Contrast](images/win7-high-contrast.png)

<span data-ttu-id="aa8a6-159">Essa imagem mostra a mesma caixa de diálogo em alto contraste no Windows 8, mas com a compatibilidade com o Windows 7 especificada no manifesto do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="aa8a6-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![W8 caixa de diálogo de alto contraste](images/win7-compat.png)

<span data-ttu-id="aa8a6-161">Essa imagem mostra a mesma caixa de diálogo em alto contraste no Windows 8, com o Windows 8 especificado no manifesto do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="aa8a6-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![caixa de diálogo de alto contraste do W8 com manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="aa8a6-163">Detectando Alto Contraste em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="aa8a6-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="aa8a6-164">Os aplicativos executados em versões anteriores do Windows não têm acesso aos novos temas de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="aa8a6-165">Se seu aplicativo precisar ser executado em versões anteriores do, você deverá incluir o suporte para renderizar sua interface do usuário em alta contraWindowsst no modelo clássico de tema do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa8a6-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="aa8a6-166">Seu aplicativo pode determinar se um tema de alto contraste está ativo chamando a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o sinalizador **SPI \_ GETHIGHCONTRAST** .</span><span class="sxs-lookup"><span data-stu-id="aa8a6-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa8a6-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8a6-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8a6-168">Habilitar estilos visuais</span><span class="sxs-lookup"><span data-stu-id="aa8a6-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="aa8a6-169">Estilos visuais</span><span class="sxs-lookup"><span data-stu-id="aa8a6-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 