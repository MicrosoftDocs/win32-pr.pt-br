---
title: Automação da Interface de Usuário
description: A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade que permite que os aplicativos do Windows forneçam e consumam informações programáticas sobre interfaces do usuário.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823891"
---
# <a name="ui-automation"></a><span data-ttu-id="bc71f-103">Automação da Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="bc71f-103">UI Automation</span></span>

<span data-ttu-id="bc71f-104">A automação da interface do usuário da Microsoft é uma estrutura de acessibilidade que permite que os aplicativos do Windows forneçam e consumam informações programáticas sobre interfaces do usuário.</span><span class="sxs-lookup"><span data-stu-id="bc71f-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="bc71f-105">Ele fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc71f-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="bc71f-106">Ele permite que produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="bc71f-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="bc71f-107">A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bc71f-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="bc71f-108">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="bc71f-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="bc71f-109">Público do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="bc71f-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="bc71f-110">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="bc71f-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="bc71f-111">Suporte para sistemas operacionais de nível inferior</span><span class="sxs-lookup"><span data-stu-id="bc71f-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="bc71f-112">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="bc71f-112">Where Applicable</span></span>

<span data-ttu-id="bc71f-113">Usando a automação da interface do usuário e as práticas de design acessíveis a seguir, os desenvolvedores podem fazer com que os aplicativos em execução no Windows sejam mais acessíveis para muitas pessoas com deficiências visuais, auditivas ou motoras.</span><span class="sxs-lookup"><span data-stu-id="bc71f-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="bc71f-114">Além disso, a automação da interface do usuário foi projetada especificamente para fornecer uma funcionalidade robusta para cenários de teste automatizados.</span><span class="sxs-lookup"><span data-stu-id="bc71f-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bc71f-115">Público do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="bc71f-115">Developer Audience</span></span>

<span data-ttu-id="bc71f-116">A automação da interface do usuário foi projetada para desenvolvedores experientes de C/C++.</span><span class="sxs-lookup"><span data-stu-id="bc71f-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="bc71f-117">Em geral, os desenvolvedores precisam de um nível moderado de compreensão sobre objetos de Component Object Model (COM) e interfaces, Unicode e programação de API do Windows.</span><span class="sxs-lookup"><span data-stu-id="bc71f-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="bc71f-118">Para obter informações sobre automação de interface do usuário para código gerenciado, consulte [acessibilidade](/dotnet/framework/ui-automation/) na seção Guia do desenvolvedor .NET Framework do MSDN.</span><span class="sxs-lookup"><span data-stu-id="bc71f-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bc71f-119">Requisitos de Run-Time</span><span class="sxs-lookup"><span data-stu-id="bc71f-119">Run-Time Requirements</span></span>

<span data-ttu-id="bc71f-120">A automação da interface do usuário tem suporte nos seguintes sistemas operacionais: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 e Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="bc71f-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="bc71f-121">O Windows XP e o Windows Server 2003 também exigem Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="bc71f-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="bc71f-122">Suporte para sistemas operacionais de nível inferior</span><span class="sxs-lookup"><span data-stu-id="bc71f-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="bc71f-123">A atualização de plataforma para o Windows Vista é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para os sistemas operacionais Windows 7 e de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="bc71f-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="bc71f-124">A atualização de plataforma para o Windows Server 2008 é um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows Server 2008 R2 e versões anteriores do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="bc71f-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="bc71f-125">A atualização da plataforma para Windows Vista e a atualização da plataforma para Windows Server 2008 estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="bc71f-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="bc71f-126">Aplicativos de terceiros que exigem atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 podem ter Windows Update detectar se estão instalados; Se não estiver, Windows Update será baixado e instalado em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bc71f-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="bc71f-127">A atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 oferecem suporte a todo o conjunto de recursos da API de automação do Windows 3,0 nos seguintes sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="bc71f-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="bc71f-128">Windows XP (inglês)</span><span class="sxs-lookup"><span data-stu-id="bc71f-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="bc71f-129">Windows XP Home SP3 x86</span><span class="sxs-lookup"><span data-stu-id="bc71f-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="bc71f-130">Windows XP Professional SP3 x86</span><span class="sxs-lookup"><span data-stu-id="bc71f-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="bc71f-131">Windows Server 2003 SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="bc71f-132">Windows Vista (inglês)</span><span class="sxs-lookup"><span data-stu-id="bc71f-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="bc71f-133">Starter SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="bc71f-134">Home Premium SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="bc71f-135">Business SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="bc71f-136">Enterprise SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="bc71f-137">Ultimate SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="bc71f-138">Windows Server 2008 (inglês)</span><span class="sxs-lookup"><span data-stu-id="bc71f-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="bc71f-139">Windows Server 2008 SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="bc71f-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="bc71f-140">Para obter mais informações sobre as duas atualizações, consulte [atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="bc71f-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bc71f-141">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bc71f-141">In this section</span></span>

-   [<span data-ttu-id="bc71f-142">Conceitos básicos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bc71f-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="bc71f-143">Guia do programador do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bc71f-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="bc71f-144">Guia do programador do cliente de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="bc71f-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="bc71f-145">Referência</span><span class="sxs-lookup"><span data-stu-id="bc71f-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="bc71f-146">Amostras</span><span class="sxs-lookup"><span data-stu-id="bc71f-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="bc71f-147">Apêndices</span><span class="sxs-lookup"><span data-stu-id="bc71f-147">Appendixes</span></span>](appendix-entry.md)

 

 