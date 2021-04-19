---
description: Saiba como usar a ferramenta de Standard User Analyzer (SUA) e o assistente de SUA para testar seus aplicativos e detectar possíveis problemas de compatibilidade.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314579"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="50c52-103">Ferramenta SUA (Standard User Analyzer) (SUA) e Assistente do SUA (Assistente do Standard User Analyzer)</span><span class="sxs-lookup"><span data-stu-id="50c52-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="50c52-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="50c52-104">Affected Platforms</span></span>

<span data-ttu-id="50c52-105">**Clientes:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="50c52-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="50c52-106">**Servidores:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50c52-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="50c52-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="50c52-107">Description</span></span>

<span data-ttu-id="50c52-108">O kit de ferramentas de compatibilidade de aplicativos inclui a ferramenta de Standard User Analyzer (SUA) e o assistente de Standard User Analyzer (Assistente de SUA).</span><span class="sxs-lookup"><span data-stu-id="50c52-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="50c52-109">Essas ferramentas permitem que você teste seus aplicativos e monitore as chamadas à API para detectar possíveis problemas de compatibilidade devido ao recurso UAC (controle de conta de usuário) no sistema operacional Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50c52-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="50c52-110">O UAC, anteriormente conhecido como LUA (conta de usuário limitada), requer que todos os usuários (incluindo membros do grupo de administradores) sejam executados como usuários padrão usando a caixa de diálogo de aviso de segurança até que o aplicativo seja deliberadamente elevado.</span><span class="sxs-lookup"><span data-stu-id="50c52-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="50c52-111">No entanto, os aplicativos que exigem acesso e privilégios para locais que não estão disponíveis para um usuário padrão não podem ser executados corretamente com a função de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="50c52-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="50c52-112">Uso</span><span class="sxs-lookup"><span data-stu-id="50c52-112">Usage</span></span>

<span data-ttu-id="50c52-113">As seções a seguir fornecem informações detalhadas sobre como usar as ferramentas do seu e do assistente de SUA.</span><span class="sxs-lookup"><span data-stu-id="50c52-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="50c52-114">**Ferramenta SUA**</span><span class="sxs-lookup"><span data-stu-id="50c52-114">**SUA Tool**</span></span>

<span data-ttu-id="50c52-115">A ferramenta SUA permite analisar um aplicativo, examinar um relatório detalhado sobre os problemas relacionados ao UAC e, em seguida, aplicar as atenuações de aplicativo sugeridas e selecionadas, conforme mostrado no fluxograma a seguir.</span><span class="sxs-lookup"><span data-stu-id="50c52-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Diagrama que mostra o fluxo do S U uma ferramenta.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="50c52-117">*Ferramenta e virtualização da SUA*</span><span class="sxs-lookup"><span data-stu-id="50c52-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="50c52-118">Somente a ferramenta SUA permite ativar e desativar o recurso de virtualização.</span><span class="sxs-lookup"><span data-stu-id="50c52-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="50c52-119">Ao desativar o recurso de virtualização, o aplicativo testado se comportará mais como quando estiver funcionando no sistema operacional Windows XP.</span><span class="sxs-lookup"><span data-stu-id="50c52-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="50c52-120">*Ferramenta SUA e privilégios elevados*</span><span class="sxs-lookup"><span data-stu-id="50c52-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="50c52-121">Somente a ferramenta SUA permite ativar e desativar o recurso de **inicialização elevada** .</span><span class="sxs-lookup"><span data-stu-id="50c52-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="50c52-122">O recurso de inicialização elevada permite que o aplicativo selecionado seja executado como administrador ou como usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="50c52-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="50c52-123">Dependendo da sua seleção, você encontrará diferentes tipos de problemas relacionados ao UAC.</span><span class="sxs-lookup"><span data-stu-id="50c52-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="50c52-124">Se você desmarcar a caixa de seleção Iniciar com privilégios **elevados** , seu aplicativo será executado com privilégios totais de administrador, o que permite ao seu prever os problemas que podem ocorrer para um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="50c52-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="50c52-125">Se você marcar a caixa de seleção Iniciar com privilégios elevados, você verá erros que resultam do aplicativo realmente executando e gerando erros.</span><span class="sxs-lookup"><span data-stu-id="50c52-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="50c52-126">**Assistente de SUA**</span><span class="sxs-lookup"><span data-stu-id="50c52-126">**SUA Wizard**</span></span>

<span data-ttu-id="50c52-127">O assistente do SUA permite que você siga um processo guiado e passo a passo pelo qual você pode analisar um aplicativo e, em seguida, aplicar as atenuações sugeridas e selecionadas do aplicativo, conforme mostrado no fluxograma a seguir.</span><span class="sxs-lookup"><span data-stu-id="50c52-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="50c52-128">Diferentemente da ferramenta do SUA, o assistente não permite uma revisão dos problemas detalhados relacionados ao UAC.</span><span class="sxs-lookup"><span data-stu-id="50c52-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Diagrama que mostra o fluxo do S U de um assistente.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="50c52-130">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="50c52-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="50c52-131">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="50c52-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="50c52-132">[Noções básicas sobre as ferramentas de Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="50c52-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="50c52-133">[Referência técnica do Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="50c52-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="50c52-134">[Testando e mitigando problemas usando as ferramentas de desenvolvimento](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="50c52-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="50c52-135">Compatibilidade de aplicativos e controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="50c52-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="50c52-136">Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.</span><span class="sxs-lookup"><span data-stu-id="50c52-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
