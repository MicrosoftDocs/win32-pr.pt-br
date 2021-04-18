---
title: Sobre a atualização da plataforma para Windows Vista
description: Fornece uma visão geral da atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008 e seus recursos.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Atualização de plataforma para o Windows Server 2008
- Atualização da plataforma para Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105764122"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="508f0-105">Sobre a atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="508f0-106">A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 são atualizações do sistema operacional do usuário final que dão suporte ao uso de tecnologias selecionadas do Windows 7 em versões anteriores do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="508f0-107">As atualizações incluem um conjunto de bibliotecas de tempo de execução que permitem que os desenvolvedores de aplicativos direcionem versões atuais, o Windows 7 e o Windows Server 2008 R2, bem como versões anteriores, o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="508f0-108">Resumo da API com suporte por tecnologia</span><span class="sxs-lookup"><span data-stu-id="508f0-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="508f0-109">Cada tecnologia com suporte da atualização da plataforma para o Windows Vista e a atualização de plataforma para atualizações do Windows Server 2008 inclui um conjunto de APIs que podem ser usadas em um aplicativo que tem como alvo a versão anterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="508f0-110">Para obter mais informações sobre como usar APIs com suporte nas atualizações em um aplicativo que tem como alvo versões anteriores do Windows, consulte [desenvolvendo aplicativos para versões anteriores do Windows](developing-applications-for-previous-versions-of-windows.md).</span><span class="sxs-lookup"><span data-stu-id="508f0-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="508f0-111">Algumas APIs que estão associadas a uma tecnologia podem não ter suporte e o comportamento, o desempenho ou os requisitos para algumas APIs com suporte podem variar em versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="508f0-112">Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="508f0-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="508f0-113">Tecnologias compatíveis com a atualização de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="508f0-114">Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="508f0-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="508f0-115">As tecnologias com suporte para o Windows Vista e o Windows XP com a atualização de plataforma para Windows Vista são mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="508f0-116">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="508f0-116">Technology</span></span>                                                                                    | <span data-ttu-id="508f0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-117">Windows Vista</span></span> | <span data-ttu-id="508f0-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="508f0-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="508f0-119">API de automação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="508f0-120">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-120">Yes</span></span>           | <span data-ttu-id="508f0-121">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-121">Yes</span></span>        |
| [<span data-ttu-id="508f0-122">Gráficos do Windows, biblioteca de imagens e XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="508f0-123">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-123">Yes</span></span>           | <span data-ttu-id="508f0-124">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-124">No</span></span>         |
| [<span data-ttu-id="508f0-125">Biblioteca de Ribbon e Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="508f0-126">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-126">Yes</span></span>           | <span data-ttu-id="508f0-127">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-127">No</span></span>         |
| [<span data-ttu-id="508f0-128">Plataforma de dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="508f0-129">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-129">Yes</span></span>           | <span data-ttu-id="508f0-130">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="508f0-131">Tecnologias com suporte com a atualização de plataforma para Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="508f0-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="508f0-132">Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="508f0-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="508f0-133">As tecnologias com suporte para o Windows Server 2008 e o Windows Server 2003 com a atualização de plataforma para Windows Server 2008 são mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="508f0-134">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="508f0-134">Technology</span></span>                                                                                    | <span data-ttu-id="508f0-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="508f0-135">Windows Server 2008</span></span> | <span data-ttu-id="508f0-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="508f0-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="508f0-137">API de automação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="508f0-138">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-138">Yes</span></span>                 | <span data-ttu-id="508f0-139">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-139">Yes</span></span>                 |
| [<span data-ttu-id="508f0-140">Gráficos do Windows, biblioteca de imagens e XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="508f0-141">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-141">Yes</span></span>                 | <span data-ttu-id="508f0-142">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-142">No</span></span>                  |
| [<span data-ttu-id="508f0-143">Biblioteca de Ribbon e Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="508f0-144">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-144">Yes</span></span>                 | <span data-ttu-id="508f0-145">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-145">No</span></span>                  |
| [<span data-ttu-id="508f0-146">Plataforma de dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="508f0-147">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-147">No</span></span>                  | <span data-ttu-id="508f0-148">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="508f0-149">Descrições da API com suporte por tecnologia</span><span class="sxs-lookup"><span data-stu-id="508f0-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="508f0-150">Para obter detalhes sobre a API com suporte para uma tecnologia específica, clique no link em uma das tabelas de resumo para ir para a seção sobre essa tecnologia.</span><span class="sxs-lookup"><span data-stu-id="508f0-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="508f0-151">API de automação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="508f0-152">Gráficos do Windows, biblioteca de imagens e XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="508f0-153">Biblioteca de Ribbon e Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="508f0-154">Plataforma de dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="508f0-155">API de automação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-155">Windows Automation API</span></span>

<span data-ttu-id="508f0-156">A API de automação do Windows 3,0 é um conjunto de DLLs e elementos de API que permitem que produtos de tecnologia assistencial (AT) forneçam melhor acesso ao computador para pessoas que têm dificuldades físicas ou cognitivas, deficiências ou deficiências.</span><span class="sxs-lookup"><span data-stu-id="508f0-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="508f0-157">Além disso, como a API de automação do Windows 3,0 permite que os aplicativos acessem e manipulem elementos da interface do usuário de outros aplicativos, trata-se de uma tecnologia ideal para implementar ferramentas automatizadas de teste.</span><span class="sxs-lookup"><span data-stu-id="508f0-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="508f0-158">O Microsoft Acessibilidade Ativa (MSAA) e a automação da interface do usuário são semelhantes, pois ambos fornecem meios para expor e coletar informações sobre elementos da interface do usuário e controles para dar suporte à acessibilidade da interface do usuário e à automação de teste de software.</span><span class="sxs-lookup"><span data-stu-id="508f0-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="508f0-159">A automação da interface do usuário é uma implementação do Windows da especificação de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="508f0-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="508f0-160">É uma tecnologia mais nova que aborda muitas das limitações do MSAA.</span><span class="sxs-lookup"><span data-stu-id="508f0-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="508f0-161">Para obter mais informações sobre a API de automação do Windows 3,0, consulte [API de automação do Windows: visão geral](/windows/desktop/WinAuto/windows-automation-api-overview).</span><span class="sxs-lookup"><span data-stu-id="508f0-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="508f0-162">A atualização de plataforma para Windows Vista e a atualização de plataforma para Windows Server 2008 dão suporte à seguinte API de automação do Windows 3,0:</span><span class="sxs-lookup"><span data-stu-id="508f0-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="508f0-163">Microsoft Acessibilidade Ativa (MSAA)</span><span class="sxs-lookup"><span data-stu-id="508f0-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="508f0-164">Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="508f0-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="508f0-165">Edições do Windows qualificadas para as atualizações</span><span class="sxs-lookup"><span data-stu-id="508f0-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="508f0-166">A atualização de plataforma para Windows Vista e a atualização de plataforma para Windows Server 2008 habilitam o suporte à API de automação do Windows 3,0 nas edições do Windows mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="508f0-167">Versão do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-167">Windows Version</span></span></th>
<th><span data-ttu-id="508f0-168">Edições qualificadas para atualização</span><span class="sxs-lookup"><span data-stu-id="508f0-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="508f0-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="508f0-170">Iniciador com SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="508f0-171">Home Basic com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-172">Home Premium com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-173">Negócios com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-174">Enterprise com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-175">Ultimate com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="508f0-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="508f0-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="508f0-177">Windows XP Home com SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="508f0-178">Windows XP Professional com SP3 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="508f0-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="508f0-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="508f0-180">Windows Server 2008 com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="508f0-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="508f0-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="508f0-182">Windows Server 2003 com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="508f0-183">Microsoft Acessibilidade Ativa (MSAA)</span><span class="sxs-lookup"><span data-stu-id="508f0-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="508f0-184">O Microsoft Acessibilidade Ativa (MSAA) é uma tecnologia herdada que foi introduzida pela primeira vez com o Windows 95.</span><span class="sxs-lookup"><span data-stu-id="508f0-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="508f0-185">É um conjunto de APIs que melhora o modo como os produtos de tecnologia assistencial (em) funcionam com aplicativos em execução no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="508f0-186">A API fornece interfaces e métodos de programação para expor informações sobre elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="508f0-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="508f0-187">Para obter mais informações sobre o Microsoft Acessibilidade Ativa, consulte a [visão geral técnica](/windows/desktop/WinAuto/technical-overview).</span><span class="sxs-lookup"><span data-stu-id="508f0-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="508f0-188">Elementos da API do Microsoft Acessibilidade Ativa com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="508f0-189">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="508f0-190">Automação da Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="508f0-190">UI Automation</span></span>

<span data-ttu-id="508f0-191">A automação da interface do usuário é uma tecnologia mais nova que implementa a especificação de automação da interface do usuário e aborda muitas das limitações do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="508f0-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="508f0-192">É um conjunto de APIs que fornece acesso programático aos elementos de interface do usuário dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="508f0-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="508f0-193">A API fornecida ajuda produtos de tecnologia assistencial e ferramentas de teste automatizadas a acessar, identificar e manipular os elementos de interface do usuário padrão e personalizados de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="508f0-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="508f0-194">Para obter mais informações sobre automação da interface do usuário, consulte [API de automação do Windows: automação da interface do usuário](../winauto/entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="508f0-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="508f0-195">Elementos da API de automação da interface do usuário com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="508f0-196">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="508f0-197">Executando a automação da interface do usuário em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="508f0-198">Devido às diferenças em como os controles comuns e os controles padrão do Windows são implementados em diferentes versões do Windows, pode haver pequenas diferenças nas informações que os proxies de automação da interface do usuário recuperam para esses controles de uma versão para outra.</span><span class="sxs-lookup"><span data-stu-id="508f0-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="508f0-199">Gráficos do Windows, biblioteca de imagens e XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="508f0-200">A atualização da plataforma para o Windows Vista dá suporte às seguintes APIs do Windows 7 a partir da biblioteca de gráficos, imagens e XPS do Windows:</span><span class="sxs-lookup"><span data-stu-id="508f0-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="508f0-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="508f0-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="508f0-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="508f0-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="508f0-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="508f0-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="508f0-204">Empacotamento</span><span class="sxs-lookup"><span data-stu-id="508f0-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="508f0-205">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="508f0-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="508f0-206">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="508f0-207">Impressão XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="508f0-208">Edições do Windows qualificadas para as atualizações</span><span class="sxs-lookup"><span data-stu-id="508f0-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="508f0-209">A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 habilitam gráficos do Windows, imagens e suporte à biblioteca XPS nas edições do Windows mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="508f0-210">Versão do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-210">Windows Version</span></span></th>
<th><span data-ttu-id="508f0-211">Edições qualificadas para atualização</span><span class="sxs-lookup"><span data-stu-id="508f0-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="508f0-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="508f0-213">Iniciador com SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="508f0-214">Home Basic com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-215">Home Premium com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-216">Negócios com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-217">Enterprise com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-218">Ultimate com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="508f0-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="508f0-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="508f0-220">Windows Server 2008 com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="508f0-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="508f0-221">Direct2D</span></span>

<span data-ttu-id="508f0-222">A API do Direct2D é uma nova API de gráficos de modo imediato e acelerada por hardware que fornece alto desempenho e renderização de alta qualidade para geometria, bitmaps e texto 2D.</span><span class="sxs-lookup"><span data-stu-id="508f0-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="508f0-223">A API Direct2D foi projetada para interoperar bem com o código existente que usa GDI, GDI+ ou Direct3D.</span><span class="sxs-lookup"><span data-stu-id="508f0-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="508f0-224">Para obter mais informações sobre o Direct2D, consulte [about Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span><span class="sxs-lookup"><span data-stu-id="508f0-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="508f0-225">Elementos da API Direct2D com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="508f0-226">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="508f0-227">Executando o Direct2D em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="508f0-228">Se o driver do WDDM 1,1 estiver faltando no Windows Vista, o desempenho da interoperabilidade Direct2D/GDI degrada.</span><span class="sxs-lookup"><span data-stu-id="508f0-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="508f0-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="508f0-229">Direct3D</span></span>

<span data-ttu-id="508f0-230">A atualização de plataforma para o Windows Vista fornece suporte de superfície BGRA para caminhos de código Direct3D10 e Direct3D 10.1.</span><span class="sxs-lookup"><span data-stu-id="508f0-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="508f0-231">O Direct3D10Level9 permite que a funcionalidade Direct3D10 funcione em hardware de Direct3D9.</span><span class="sxs-lookup"><span data-stu-id="508f0-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="508f0-232">O Direct3D WARP10 é um rasterizador de software de alto desempenho para aplicativos Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="508f0-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="508f0-233">O Direct3D11, a versão mais recente do Direct3D, fornece novos recursos, como suporte a multithread aprimorado, mosaico, funcionalidade de DirectCompute e vinculação dinâmica de sombreador.</span><span class="sxs-lookup"><span data-stu-id="508f0-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="508f0-234">Se você criar aplicativos que usam o Direct3D, o [SDK do DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) é necessário.</span><span class="sxs-lookup"><span data-stu-id="508f0-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="508f0-235">Para obter mais informações sobre o Direct3D, consulte [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="508f0-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="508f0-236">Elementos de API do Direct3D com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="508f0-237">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="508f0-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="508f0-238">DirectWrite</span></span>

<span data-ttu-id="508f0-239">A API DirectWrite é uma nova API de texto que fornece várias camadas de funcionalidade, incluindo layout de texto, processamento de scripts, renderização de glifos e sistema de fontes.</span><span class="sxs-lookup"><span data-stu-id="508f0-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="508f0-240">O DirectWrite usa fontes OpenType e renderização de ClearType de sub-pixel para aprimorar a experiência de texto fornecida pelos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="508f0-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="508f0-241">A renderização de texto é acelerada pelo hardware quando usada com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="508f0-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="508f0-242">Para obter mais informações sobre DirectWrite, consulte [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span><span class="sxs-lookup"><span data-stu-id="508f0-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="508f0-243">Elementos da API DirectWrite com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="508f0-244">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="508f0-245">Executando o DirectWrite em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="508f0-246">Os seguintes problemas comportamentais podem afetar o uso da API DirectWrite em versões anteriores do Windows:</span><span class="sxs-lookup"><span data-stu-id="508f0-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="508f0-247">Os scripts novos para o Windows 7 podem não ser renderizados totalmente corretamente em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="508f0-248">As localidades não disponíveis nas versões anteriores do Windows retornam ao comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="508f0-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="508f0-249">O sintonizador ClearType não está disponível em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="508f0-250">A interoperabilidade GDI tem um custo de memória maior em alguns cenários em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="508f0-251">Empacotamento</span><span class="sxs-lookup"><span data-stu-id="508f0-251">Packaging</span></span>

<span data-ttu-id="508f0-252">A atualização de plataforma para o Windows Vista dá suporte a um subconjunto limitado de APIs de empacotamento que são necessárias para executar tarefas com a API de documento XPS em aplicativos não gerenciados.</span><span class="sxs-lookup"><span data-stu-id="508f0-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="508f0-253">Para obter mais informações sobre APIs de empacotamento, consulte a [visão geral da API de empacotamento](/previous-versions/windows/desktop/opc/packaging-api-overview).</span><span class="sxs-lookup"><span data-stu-id="508f0-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="508f0-254">Elementos da API de empacotamento com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="508f0-255">Há suporte apenas para as seguintes interfaces de empacotamento:</span><span class="sxs-lookup"><span data-stu-id="508f0-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="508f0-256">IOpcUri</span><span class="sxs-lookup"><span data-stu-id="508f0-256">IOpcUri</span></span>
-   <span data-ttu-id="508f0-257">IOpcPartUri</span><span class="sxs-lookup"><span data-stu-id="508f0-257">IOpcPartUri</span></span>
-   <span data-ttu-id="508f0-258">IOpcFactory (há suporte apenas para os métodos a seguir)</span><span class="sxs-lookup"><span data-stu-id="508f0-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="508f0-259">CreatePackageRootUri</span><span class="sxs-lookup"><span data-stu-id="508f0-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="508f0-260">CreatePartUri</span><span class="sxs-lookup"><span data-stu-id="508f0-260">CreatePartUri</span></span>
    -   <span data-ttu-id="508f0-261">CreateStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="508f0-261">CreateStreamOnFile</span></span>

<span data-ttu-id="508f0-262">APIs de empacotamento com suporte podem ser usadas para criar fluxos em arquivos, bem como para criar e interagir com o URI baseado em pacote.</span><span class="sxs-lookup"><span data-stu-id="508f0-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="508f0-263">Executando a API de empacotamento em versões anteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="508f0-264">O comportamento e o desempenho de interfaces e métodos de empacotamento com suporte são os mesmos em todas as plataformas com suporte.</span><span class="sxs-lookup"><span data-stu-id="508f0-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="508f0-265">Se um aplicativo tentar instanciar ou chamar uma interface ou um método de empacotamento sem suporte, a tentativa falhará.</span><span class="sxs-lookup"><span data-stu-id="508f0-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="508f0-266">Se a chamada for para um método [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) sem suporte, o código de \_ erro E NOTIMPL será retornado.</span><span class="sxs-lookup"><span data-stu-id="508f0-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="508f0-267">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="508f0-267">Windows Imaging Component</span></span>

<span data-ttu-id="508f0-268">Os novos recursos do Windows Imaging Component (WIC) incluem segurança aprimorada, suporte para alta cor e melhor interoperabilidade de metadados.</span><span class="sxs-lookup"><span data-stu-id="508f0-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="508f0-269">Além disso, o Windows Imaging Component amplia sua conformidade com os padrões fornecendo suporte para decodificação de imagem progressiva, recursos de PNG expandidos, metadados GIF, atualizações de foto de HD e metadados que abrangem segmentos APPn.</span><span class="sxs-lookup"><span data-stu-id="508f0-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="508f0-270">Para obter mais informações sobre o Windows Imaging Component, consulte a [visão geral do Windows Imaging Component](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span><span class="sxs-lookup"><span data-stu-id="508f0-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="508f0-271">Elementos de API do WIC com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-271">Supported WIC API Elements</span></span>

<span data-ttu-id="508f0-272">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="508f0-273">Documento XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-273">XPS Document</span></span>

<span data-ttu-id="508f0-274">As APIs de documento XPS dão suporte à criação, modificação e salvamento de documentos XPS em aplicativos não gerenciados</span><span class="sxs-lookup"><span data-stu-id="508f0-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="508f0-275">Para obter mais informações sobre APIs de documento XPS, consulte o [Guia de programação de documento XPS.](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="508f0-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="508f0-276">Elementos de API de documento XPS com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="508f0-277">Somente as interfaces de [assinaturas digitais XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) não têm suporte em versões de sistema operacional de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="508f0-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="508f0-278">Impressão XPS</span><span class="sxs-lookup"><span data-stu-id="508f0-278">XPS Print</span></span>

<span data-ttu-id="508f0-279">As APIs de impressão do XPS dão suporte à impressão de documentos XPS de aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="508f0-280">Para obter mais informações sobre APIs de impressão do XPS, consulte a [API do XpsPrint](/windows/desktop/printdocs/xpsprint-api).</span><span class="sxs-lookup"><span data-stu-id="508f0-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="508f0-281">Elementos da API de impressão XPS com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="508f0-282">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="508f0-283">Biblioteca de Ribbon e Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="508f0-284">A atualização da plataforma para o Windows Vista dá suporte às seguintes APIs do Windows 7 na faixa de opções e na biblioteca de animações do Windows:</span><span class="sxs-lookup"><span data-stu-id="508f0-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="508f0-285">Estrutura da faixa de dasgem do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="508f0-286">Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="508f0-287">Edições do Windows qualificadas para as atualizações</span><span class="sxs-lookup"><span data-stu-id="508f0-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="508f0-288">A atualização da plataforma para o Windows Vista e a atualização da plataforma para o Windows Server 2008 habilite o suporte da faixa de opções do Windows e da biblioteca do Gerenciador de animação nas edições do Windows mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="508f0-289">Versão do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-289">Windows Version</span></span></th>
<th><span data-ttu-id="508f0-290">Edições qualificadas para atualização</span><span class="sxs-lookup"><span data-stu-id="508f0-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="508f0-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="508f0-292">Iniciador com SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="508f0-293">Home Basic com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-294">Home Premium com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-295">Negócios com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-296">Enterprise com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-297">Ultimate com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="508f0-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="508f0-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="508f0-299">Windows Server 2008 com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="508f0-300">Estrutura da faixa de dasgem do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="508f0-301">A estrutura de faixa de ferramentas do Windows (faixa de ferramentas) é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de tarefas e painéis de tarefa de aplicativos tradicionais do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="508f0-302">A estrutura é uma coleção de APIs do Microsoft Win32 que fornece um host de novos recursos de interface do usuário para desenvolvedores do Windows e inclui a faixa de opções e um sistema de menus de contexto.</span><span class="sxs-lookup"><span data-stu-id="508f0-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="508f0-303">Para obter mais informações sobre a estrutura da faixa de faixas, consulte [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="508f0-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="508f0-304">Elementos da API da estrutura da faixa de faixas com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="508f0-305">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="508f0-306">Gerenciador de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-306">Windows Animation Manager</span></span>

<span data-ttu-id="508f0-307">O Windows Animation Manager (animação do Windows) é uma interface programática que dá suporte à animação de elementos visuais de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="508f0-308">A animação do Windows foi projetada para simplificar o desenvolvimento e a manutenção de sequências de animação e permitir que os desenvolvedores implementem animações que são consistentes e intuitivas.</span><span class="sxs-lookup"><span data-stu-id="508f0-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="508f0-309">A animação do Windows pode ser usada com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.</span><span class="sxs-lookup"><span data-stu-id="508f0-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="508f0-310">A animação do Windows é uma API COM de thread único que fornece tudo o que um desenvolvedor precisa para criar, gerenciar e orientar a animação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="508f0-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="508f0-311">Para obter mais informações sobre o Gerenciador de animação do Windows, consulte [introdução à animação do Windows](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span><span class="sxs-lookup"><span data-stu-id="508f0-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="508f0-312">Elementos da API do Gerenciador de animação com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="508f0-313">Todas as APIs têm suporte em versões anteriores do Windows qualificadas para a atualização de plataforma para o Windows Vista ou a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="508f0-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="508f0-314">Plataforma de dispositivos portáteis do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="508f0-315">A atualização da plataforma para o Windows Vista dá suporte às extensões do Windows 7 para a plataforma de dispositivos portáteis do Windows (WPD).</span><span class="sxs-lookup"><span data-stu-id="508f0-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="508f0-316">Esse recurso permite que os computadores se comuniquem com dispositivos de mídia e armazenamento anexados.</span><span class="sxs-lookup"><span data-stu-id="508f0-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="508f0-317">O WPD fornece uma maneira flexível e robusta para que os computadores se comuniquem com câmeras digitais, players de música, celulares e muitos outros tipos de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="508f0-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="508f0-318">Para obter mais informações sobre dispositivos portáteis do Windows, consulte [dispositivos portáteis do Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .</span><span class="sxs-lookup"><span data-stu-id="508f0-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="508f0-319">Edições do Windows qualificadas para as atualizações</span><span class="sxs-lookup"><span data-stu-id="508f0-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="508f0-320">A atualização da plataforma para o Windows Vista e a atualização da plataforma para Windows Server 2008 habilitam o suporte a dispositivos portáteis do Windows (WPD) nas edições do Windows mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="508f0-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="508f0-321">Versão do Windows</span><span class="sxs-lookup"><span data-stu-id="508f0-321">Windows Version</span></span></th>
<th><span data-ttu-id="508f0-322">Edições qualificadas para atualização</span><span class="sxs-lookup"><span data-stu-id="508f0-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="508f0-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="508f0-324">Iniciador com SP2 (x86)</span><span class="sxs-lookup"><span data-stu-id="508f0-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="508f0-325">Home Basic com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-326">Home Premium com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-327">Negócios com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-328">Enterprise com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="508f0-329">Ultimate com SP2 (x86 e AMD64)</span><span class="sxs-lookup"><span data-stu-id="508f0-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="508f0-330">Elementos de API WPD com suporte</span><span class="sxs-lookup"><span data-stu-id="508f0-330">Supported WPD API Elements</span></span>

<span data-ttu-id="508f0-331">A tabela a seguir identifica os recursos com suporte para o Windows 7, Windows Vista e Windows Vista com a atualização de plataforma para versões do Windows Vista do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="508f0-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="508f0-332">Recurso WPD</span><span class="sxs-lookup"><span data-stu-id="508f0-332">WPD Feature</span></span>                    | <span data-ttu-id="508f0-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="508f0-333">Windows 7</span></span> | <span data-ttu-id="508f0-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-334">Windows Vista</span></span> | <span data-ttu-id="508f0-335">Windows Vista com atualização de plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="508f0-336">MTP sobre USB</span><span class="sxs-lookup"><span data-stu-id="508f0-336">MTP over USB</span></span>                   | <span data-ttu-id="508f0-337">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-337">Yes</span></span>       | <span data-ttu-id="508f0-338">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-338">Yes</span></span>           | <span data-ttu-id="508f0-339">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-339">Yes</span></span>                                                  |
| <span data-ttu-id="508f0-340">MTP sobre IP</span><span class="sxs-lookup"><span data-stu-id="508f0-340">MTP over IP</span></span>                    | <span data-ttu-id="508f0-341">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-341">Yes</span></span>       | <span data-ttu-id="508f0-342">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-342">Yes</span></span>           | <span data-ttu-id="508f0-343">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-343">Yes</span></span>                                                  |
| <span data-ttu-id="508f0-344">MTP em Bluetooth</span><span class="sxs-lookup"><span data-stu-id="508f0-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="508f0-345">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-345">Yes</span></span>       | <span data-ttu-id="508f0-346">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-346">No</span></span>            | <span data-ttu-id="508f0-347">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-347">Yes</span></span>                                                  |
| <span data-ttu-id="508f0-348">Serviços de dispositivos WPD e MTP</span><span class="sxs-lookup"><span data-stu-id="508f0-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="508f0-349">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-349">Yes</span></span>       | <span data-ttu-id="508f0-350">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-350">No</span></span>            | <span data-ttu-id="508f0-351">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-351">Yes</span></span>                                                  |
| <span data-ttu-id="508f0-352">Automação WPD</span><span class="sxs-lookup"><span data-stu-id="508f0-352">WPD Automation</span></span>                 | <span data-ttu-id="508f0-353">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-353">Yes</span></span>       | <span data-ttu-id="508f0-354">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-354">No</span></span>            | <span data-ttu-id="508f0-355">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-355">No</span></span>                                                   |
| <span data-ttu-id="508f0-356">Multifuncional/multi-transporte</span><span class="sxs-lookup"><span data-stu-id="508f0-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="508f0-357">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-357">Yes</span></span>       | <span data-ttu-id="508f0-358">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-358">No</span></span>            | <span data-ttu-id="508f0-359">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-359">No</span></span>                                                   |
| <span data-ttu-id="508f0-360">Device Stage</span><span class="sxs-lookup"><span data-stu-id="508f0-360">Device Stage</span></span>                   | <span data-ttu-id="508f0-361">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-361">Yes</span></span>       | <span data-ttu-id="508f0-362">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-362">No</span></span>            | <span data-ttu-id="508f0-363">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-363">No</span></span>                                                   |
| <span data-ttu-id="508f0-364">Plataforma de sincronização de dispositivo</span><span class="sxs-lookup"><span data-stu-id="508f0-364">Device Sync Platform</span></span>           | <span data-ttu-id="508f0-365">Sim</span><span class="sxs-lookup"><span data-stu-id="508f0-365">Yes</span></span>       | <span data-ttu-id="508f0-366">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-366">No</span></span>            | <span data-ttu-id="508f0-367">Não</span><span class="sxs-lookup"><span data-stu-id="508f0-367">No</span></span>                                                   |



 

<span data-ttu-id="508f0-368">Para edições do Windows 7 e do Windows Vista que não têm o Microsoft Windows Media Player instalado por padrão (as edições N e KN), você deve instalar o [SDK do Windows Media Format 11]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) para habilitar a funcionalidade WPD.</span><span class="sxs-lookup"><span data-stu-id="508f0-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="508f0-369">Para obter mais informações, consulte o [artigo da base de dados de conhecimento](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , que foi publicado originalmente como uma resolução para o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="508f0-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="508f0-370">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="508f0-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="508f0-371">Atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="508f0-372">**Visões gerais**</span><span class="sxs-lookup"><span data-stu-id="508f0-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="508f0-373">Sobre a atualização da plataforma para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="508f0-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="508f0-374">Artigo da base de dados de conhecimento sobre a atualização da plataforma para Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="508f0-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 