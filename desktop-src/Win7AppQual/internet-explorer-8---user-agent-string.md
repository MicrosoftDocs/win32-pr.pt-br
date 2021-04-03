---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-cadeia de caracteres do agente do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828815"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="d7896-103">Internet Explorer 8-cadeia de caracteres do agente do usuário</span><span class="sxs-lookup"><span data-stu-id="d7896-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d7896-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="d7896-104">Affected Platforms</span></span>

 <span data-ttu-id="d7896-105">**Clientes** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="d7896-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="d7896-106">**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7896-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="d7896-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="d7896-107">Feature Impact</span></span>

<span data-ttu-id="d7896-108">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="d7896-108">**Severity** - Medium</span></span>  
<span data-ttu-id="d7896-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="d7896-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="d7896-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7896-110">Description</span></span>

<span data-ttu-id="d7896-111">A cadeia de caracteres do agente do usuário é o identificador do Internet Explorer que fornece dados sobre sua versão e outros atributos para servidores Web.</span><span class="sxs-lookup"><span data-stu-id="d7896-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="d7896-112">Muitos aplicativos Web dependem e se acumulam na cadeia de caracteres do agente do usuário do IE.</span><span class="sxs-lookup"><span data-stu-id="d7896-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="d7896-113">Os que fazem isso e dependem de um número de versão anterior serão afetados.</span><span class="sxs-lookup"><span data-stu-id="d7896-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="d7896-114">A cadeia de caracteres do agente do usuário agora inclui a cadeia de caracteres "Trident/4.0" para permitir a diferenciação entre a cadeia de caracteres do agente do usuário do Internet Explorer 7 e a cadeia de caracteres do agente do usuário do Internet Explorer 8 ao executar na exibição de compatibilidade do Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="d7896-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="d7896-115">Consulte Noções básicas sobre cadeias de agente do usuário para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="d7896-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d7896-116">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="d7896-116">Manifestation of Impact</span></span>

<span data-ttu-id="d7896-117">Há duas áreas afetadas:</span><span class="sxs-lookup"><span data-stu-id="d7896-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="d7896-118">As páginas da Web que verificam explicitamente a cadeia de caracteres do agente do usuário e não dão suporte à cadeia de caracteres do agente do usuário do Internet Explorer 8 podem não ser executadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="d7896-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="d7896-119">Na maioria dos casos, isso significa que as páginas serão bloquear os usuários do conteúdo que estão tentando acessar ou exibir conteúdo incorreto ou malformado.</span><span class="sxs-lookup"><span data-stu-id="d7896-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="d7896-120">Os aplicativos que hospedam o Trident (consulte hospedagem e reutilização) serão padronizados para o Internet Explorer 7 usando o componente opcional da Web, mas não terão acesso aos recursos do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="d7896-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="d7896-121">Solução</span><span class="sxs-lookup"><span data-stu-id="d7896-121">Solution</span></span>

<span data-ttu-id="d7896-122">Verifique se seus aplicativos manipulam corretamente a nova versão ' MSIE 8,0 ' na cadeia de caracteres do agente do usuário.</span><span class="sxs-lookup"><span data-stu-id="d7896-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="d7896-123">Você também pode optar pelo modo de exibição de compatibilidade do Internet Explorer 7 para esses aplicativos com base no Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="d7896-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="d7896-124">Isso pode ser feito com marcas meta.</span><span class="sxs-lookup"><span data-stu-id="d7896-124">This can be done with meta tags.</span></span> <span data-ttu-id="d7896-125">Consulte a discussão em Noções básicas sobre cadeias de caracteres do agente do usuário para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="d7896-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="d7896-126">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="d7896-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="d7896-127">Execute seus aplicativos e páginas da Web em um ambiente do Internet Explorer 8 no Windows Vista ou no Windows XP para garantir que eles se comportem da maneira desejada.</span><span class="sxs-lookup"><span data-stu-id="d7896-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="d7896-128">Como alternativa, você pode executar a ferramenta de teste de compatibilidade do Internet Explorer (IECTT) fornecida com o kit de ferramentas de compatibilidade de aplicativos (ACT) para localizar possíveis problemas devido a atualizações de recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="d7896-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d7896-129">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="d7896-129">Links to Other Resources</span></span>

-   <span data-ttu-id="d7896-130">[Noções básicas sobre cadeias de agente do usuário](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7896-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="d7896-131">Cadeia de caracteres User-Agent do Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="d7896-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="d7896-132">Cadeia de caracteres do agente do usuário e vetor de versão</span><span class="sxs-lookup"><span data-stu-id="d7896-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="d7896-133">[Hospedagem e reutilização](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7896-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="d7896-134">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="d7896-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="d7896-135">[Problemas conhecidos do recurso de segurança do Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="d7896-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
