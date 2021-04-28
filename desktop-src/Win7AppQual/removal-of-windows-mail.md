---
description: Remoção do Windows Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Remoção do Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116274"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="1e61a-103">Remoção do Windows Mail</span><span class="sxs-lookup"><span data-stu-id="1e61a-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="1e61a-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="1e61a-104">Affected Platforms</span></span>

<span data-ttu-id="1e61a-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e61a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1e61a-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e61a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1e61a-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="1e61a-107">Feature Impact</span></span>

<span data-ttu-id="1e61a-108">**Severidade** -alta</span><span class="sxs-lookup"><span data-stu-id="1e61a-108">**Severity** - High</span></span>  
<span data-ttu-id="1e61a-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="1e61a-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="1e61a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e61a-110">Description</span></span>

<span data-ttu-id="1e61a-111">A Microsoft está preterindo o utilitário Windows Mail e desabilitando a API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="1e61a-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="1e61a-112">As outras APIs de email foram marcadas como preteridas e são removidas para remoção em uma versão posterior do Windows.</span><span class="sxs-lookup"><span data-stu-id="1e61a-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="1e61a-113">No entanto, as APIs documentadas publicamente que não estão marcadas como preteridas ou obsoletas continuarão a funcionar no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1e61a-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="1e61a-114">Os binários permanecerão nos sistemas dos usuários e continuarão acessíveis por meio das APIs, especificamente nos casos mencionados acima.</span><span class="sxs-lookup"><span data-stu-id="1e61a-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="1e61a-115">Além disso, os arquivos de email (. eml) e de notícias (. NWS) dos usuários permanecerão no sistema.</span><span class="sxs-lookup"><span data-stu-id="1e61a-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="1e61a-116">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="1e61a-116">Manifestation of Impact</span></span>

<span data-ttu-id="1e61a-117">A remoção do Windows Mail resulta no seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e61a-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="1e61a-118">Todos os pontos de entrada para o Windows Mail e contatos (por exemplo, menu Iniciar, atalhos criados pelo usuário, execução de > de início e assim por diante) são removidos ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="1e61a-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="1e61a-119">Algumas delas são completamente removidas, outras falharão ao tentar iniciar.</span><span class="sxs-lookup"><span data-stu-id="1e61a-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="1e61a-120">Todas as DLLs são fornecidas na caixa</span><span class="sxs-lookup"><span data-stu-id="1e61a-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="1e61a-121">APIs documentadas publicamente continuam funcionando como faziam no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e61a-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="1e61a-122">Todas as APIs que tentarem iniciar a interface do usuário do navegador principal foram modificadas para criar uma falha silenciosa.</span><span class="sxs-lookup"><span data-stu-id="1e61a-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="1e61a-123">A função retornará êxito, mas não mostrará a IU ao usuário.</span><span class="sxs-lookup"><span data-stu-id="1e61a-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="1e61a-124">As APIs que chamam outras caixas de diálogo (por exemplo, o spooler ou a caixa de diálogo contas) continuam a mostrar essa interface do usuário</span><span class="sxs-lookup"><span data-stu-id="1e61a-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="1e61a-125">Os manipuladores de protocolo (mailto, LDAP, News, snews, NNTP) não serão associados ao Windows mail ou aos contatos.</span><span class="sxs-lookup"><span data-stu-id="1e61a-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="1e61a-126">Ao tentar iniciá-los, os clientes verão uma caixa de diálogo de erro apontando para o local onde podem definir essas associações para outro programa</span><span class="sxs-lookup"><span data-stu-id="1e61a-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="1e61a-127">As associações de arquivo (. eml,. nws,. Contact,. Group,. wab,. p7c,. VFC) estão desfeitas ou desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1e61a-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="1e61a-128">Ao tentar abrir um arquivo com essas extensões, os clientes receberão uma caixa de diálogo oferecendo a eles outros aplicativos instalados que podem usá-los e apontar para uma página da Web que oferece soluções</span><span class="sxs-lookup"><span data-stu-id="1e61a-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="1e61a-129">Todos os arquivos de usuário (por exemplo, arquivos de contato ou mensagens) permanecem no sistema no cenário de atualização</span><span class="sxs-lookup"><span data-stu-id="1e61a-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="1e61a-130">A pasta contatos fica oculta por padrão, de modo que os clientes não as verão</span><span class="sxs-lookup"><span data-stu-id="1e61a-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="1e61a-131">As APIs são marcadas como preteridas no MSDN</span><span class="sxs-lookup"><span data-stu-id="1e61a-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="1e61a-132">A função de visualização de arquivo foi removida</span><span class="sxs-lookup"><span data-stu-id="1e61a-132">The file preview function is removed</span></span>
-   <span data-ttu-id="1e61a-133">Os ganchos do Shell no menu de atalho são removidos</span><span class="sxs-lookup"><span data-stu-id="1e61a-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="1e61a-134">A função de pesquisa de arquivo foi removida</span><span class="sxs-lookup"><span data-stu-id="1e61a-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="1e61a-135">Atenuação</span><span class="sxs-lookup"><span data-stu-id="1e61a-135">Mitigation</span></span>

<span data-ttu-id="1e61a-136">Os usuários devem instalar o Windows Live mail ou qualquer outro produto de email capaz de ler arquivos. eml e. nws.</span><span class="sxs-lookup"><span data-stu-id="1e61a-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="1e61a-137">Solução</span><span class="sxs-lookup"><span data-stu-id="1e61a-137">Solution</span></span>

<span data-ttu-id="1e61a-138">Detectar se há um manipulador de email padrão instalado.</span><span class="sxs-lookup"><span data-stu-id="1e61a-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="1e61a-139">Caso contrário, avise o usuário para instalar o Windows Live mail ou qualquer outro produto capaz de ler arquivos. eml e. nws.</span><span class="sxs-lookup"><span data-stu-id="1e61a-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="1e61a-140">Não crie um código que chame a API da interface do usuário do Windows Mail, pois ele não funcionará.</span><span class="sxs-lookup"><span data-stu-id="1e61a-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="1e61a-141">Você deve encontrar outras maneiras de acessar os arquivos. eml e. nws.</span><span class="sxs-lookup"><span data-stu-id="1e61a-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="1e61a-142">Além disso, assim que for viável, descontinue sua dependência em todas as outras APIs do Windows Mail.</span><span class="sxs-lookup"><span data-stu-id="1e61a-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="1e61a-143">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="1e61a-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="1e61a-144">Exerça seu aplicativo em um ambiente do Windows 7 para garantir que o aplicativo não tente chamar a API da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e61a-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="1e61a-145">Como alternativa, você pode executar o kit de ferramentas de compatibilidade de aplicativos (ACT) usando o Stone (avaliador de compatibilidade do Windows) para localizar possíveis problemas devido à reprovação dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="1e61a-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1e61a-146">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="1e61a-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="1e61a-147">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="1e61a-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
