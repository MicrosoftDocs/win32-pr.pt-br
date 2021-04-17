---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interface do usuário – reconhecimento de DPI alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812028"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="ff99d-103">Interface do usuário – reconhecimento de DPI alto</span><span class="sxs-lookup"><span data-stu-id="ff99d-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ff99d-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="ff99d-104">Affected Platforms</span></span>

 <span data-ttu-id="ff99d-105">**Clientes** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="ff99d-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="ff99d-106">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="ff99d-106">Feature Impact</span></span>

<span data-ttu-id="ff99d-107">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="ff99d-107">**Severity** - Medium</span></span>  
<span data-ttu-id="ff99d-108">**Frequência** -média</span><span class="sxs-lookup"><span data-stu-id="ff99d-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="ff99d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff99d-109">Description</span></span>

<span data-ttu-id="ff99d-110">O objetivo é incentivar os usuários finais a definir seus monitores para resolução nativa e usar DPI em vez de resolução de tela para alterar o tamanho do texto e das imagens exibidas.</span><span class="sxs-lookup"><span data-stu-id="ff99d-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="ff99d-111">O Windows 7 pode detectar e configurar automaticamente um DPI padrão em instalações limpas em computadores configurados por seus OEMs usando configurações de DPI.</span><span class="sxs-lookup"><span data-stu-id="ff99d-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="ff99d-112">Há ferramentas que você pode usar para ajudar a criar aplicativos com reconhecimento de DPI alto para garantir os resultados mais legíveis.</span><span class="sxs-lookup"><span data-stu-id="ff99d-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="ff99d-113">Adicionamos dois novos recursos de DPI alto ao Windows 7:</span><span class="sxs-lookup"><span data-stu-id="ff99d-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="ff99d-114">Configuração de DPI por usuário (anteriormente por computador)</span><span class="sxs-lookup"><span data-stu-id="ff99d-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="ff99d-115">Alterar DPI sem reinicialização (o logoff/logon ainda é necessário)</span><span class="sxs-lookup"><span data-stu-id="ff99d-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ff99d-116">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="ff99d-116">Manifestation of Impact</span></span>

<span data-ttu-id="ff99d-117">Os aplicativos que não manipulam o caso de DPI alto provavelmente apresentarão artefatos visuais, incluindo:</span><span class="sxs-lookup"><span data-stu-id="ff99d-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="ff99d-118">Recorte da interface do usuário ou do texto por outros elementos da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ff99d-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="ff99d-119">Tamanhos de fonte inconsistentes</span><span class="sxs-lookup"><span data-stu-id="ff99d-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="ff99d-120">UIs fora da tela</span><span class="sxs-lookup"><span data-stu-id="ff99d-120">Off-screen UIs</span></span>
-   <span data-ttu-id="ff99d-121">Desfoque do texto ou da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ff99d-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="ff99d-122">Arrastar e soltar desfeito ou outras entradas</span><span class="sxs-lookup"><span data-stu-id="ff99d-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="ff99d-123">Renderização de aplicativos DX de tela inteira parcialmente fora da tela</span><span class="sxs-lookup"><span data-stu-id="ff99d-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="ff99d-124">Solução</span><span class="sxs-lookup"><span data-stu-id="ff99d-124">Solution</span></span>

<span data-ttu-id="ff99d-125">Para tornar seus aplicativos cientes de DPI:</span><span class="sxs-lookup"><span data-stu-id="ff99d-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="ff99d-126">Faça um passo de teste funcional de alto nível, incluindo instalar e desinstalar nas seguintes configurações:</span><span class="sxs-lookup"><span data-stu-id="ff99d-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="ff99d-127">Configuração</span><span class="sxs-lookup"><span data-stu-id="ff99d-127">Setting</span></span>                                              | <span data-ttu-id="ff99d-128">O que procurar</span><span class="sxs-lookup"><span data-stu-id="ff99d-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ff99d-129">1024x768 @ 120 DPI (125% de dimensionamento)</span><span class="sxs-lookup"><span data-stu-id="ff99d-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="ff99d-130">Essa é uma resolução efetiva de ~ 800x600, então procure a interface do usuário recortada da tela ou dos problemas de layout.</span><span class="sxs-lookup"><span data-stu-id="ff99d-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="ff99d-131">Procure também bitmaps do pixilated & ícones.</span><span class="sxs-lookup"><span data-stu-id="ff99d-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="ff99d-132">@144dpi 1600x1200 (150% de dimensionamento)</span><span class="sxs-lookup"><span data-stu-id="ff99d-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="ff99d-133">Interface do usuário borrada.</span><span class="sxs-lookup"><span data-stu-id="ff99d-133">Blurry UI.</span></span> <span data-ttu-id="ff99d-134">Verifique se todas as operações do mouse funcionam, especialmente arraste & operações drop.</span><span class="sxs-lookup"><span data-stu-id="ff99d-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="ff99d-135">Verifique também se os modos de tela inteira funcionam corretamente.</span><span class="sxs-lookup"><span data-stu-id="ff99d-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="ff99d-136">1600x1200 @ 144 DPI com virtualização de DPI desabilitada</span><span class="sxs-lookup"><span data-stu-id="ff99d-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="ff99d-137">Frequentemente, os botões e a interface do usuário não serão dimensionados em relação ao texto maior & haverá um recorte de texto significativo.</span><span class="sxs-lookup"><span data-stu-id="ff99d-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="ff99d-138">Procure problemas de layout em geral & pixilated bitmats & ícones.</span><span class="sxs-lookup"><span data-stu-id="ff99d-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="ff99d-139">Anote todos os problemas encontrados, incluindo a localização, a resolução da tela e as configurações de DPI, além de como o aplicativo se comporta nas outras configurações de DPI/resolução para fins de integridade</span><span class="sxs-lookup"><span data-stu-id="ff99d-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="ff99d-140">Verificar cada problema em relação aos problemas comuns de codificação de DPI</span><span class="sxs-lookup"><span data-stu-id="ff99d-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="ff99d-141">Avaliar o custo de fazer com que o aplicativo reconheça totalmente o DPI</span><span class="sxs-lookup"><span data-stu-id="ff99d-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="ff99d-142">Faça uma lista dos ativos de DPI alto necessários (por exemplo, botões, ícones)</span><span class="sxs-lookup"><span data-stu-id="ff99d-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="ff99d-143">Solucionar e corrigir a lista de problemas de DPI encontrados na etapa 1</span><span class="sxs-lookup"><span data-stu-id="ff99d-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="ff99d-144">Integre os novos ativos da etapa 5</span><span class="sxs-lookup"><span data-stu-id="ff99d-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="ff99d-145">Declarar o reconhecimento de DPI de aplicativo</span><span class="sxs-lookup"><span data-stu-id="ff99d-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="ff99d-146">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="ff99d-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="ff99d-147">Execute novamente a avaliação de reconhecimento de DPI e verifique se os problemas foram corrigidos.</span><span class="sxs-lookup"><span data-stu-id="ff99d-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ff99d-148">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="ff99d-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="ff99d-149">Desenvolvimento de aplicativos de desktop de alto DPI no Windows</span><span class="sxs-lookup"><span data-stu-id="ff99d-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="ff99d-150">**Contate as perguntas técnicas:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="ff99d-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
