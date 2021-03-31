---
description: .
ms.assetid: 3F79CF5F-416D-4C06-AAAE-D935F36CD2E2
title: Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ab869be07e5578d265db2e8e85147c213e1e17e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171983"
---
# <a name="addressing-application-compatibility-when-migrating-to-internet-explorer-8"></a><span data-ttu-id="49b9f-103">Abordando a compatibilidade de aplicativos ao migrar para o Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="49b9f-103">Addressing Application Compatibility When Migrating to Internet Explorer 8</span></span>

<span data-ttu-id="49b9f-104">Esta seção fornece uma visão geral do teste de problemas de compatibilidade de aplicativos e correção desses problemas em aplicativos Web para o Windows Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="49b9f-104">This section provides an overview of testing for application compatibility issues and fixing those issues in web applications for Windows Internet Explorer 8.</span></span> <span data-ttu-id="49b9f-105">Os tópicos a seguir descrevem as alterações no Internet Explorer 8 e as ferramentas e tecnologias para garantir a compatibilidade do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49b9f-105">The following topics describe the changes in Internet Explorer 8 and the tools and technologies to ensure compatibility for your application.</span></span>



| <span data-ttu-id="49b9f-106">Seção</span><span class="sxs-lookup"><span data-stu-id="49b9f-106">Section</span></span>                                                                                                                                              | <span data-ttu-id="49b9f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="49b9f-107">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49b9f-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="49b9f-108">Introduction</span></span>](introduction.md)                                                                                                                     | <span data-ttu-id="49b9f-109">Fornece uma visão geral das considerações de compatibilidade do Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="49b9f-109">Provides an overview of Internet Explorer 8 compatibility considerations.</span></span>                 |
| [<span data-ttu-id="49b9f-110">Noções básicas sobre o desafio da compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="49b9f-110">Understanding the Application Compatibility Challenge</span></span>](understanding-the-application-compatibility-challenge.md)                                   | <span data-ttu-id="49b9f-111">Fornece informações sobre a compatibilidade com o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="49b9f-111">Provides background about Internet Explorer 8 compatibility.</span></span>                              |
| [<span data-ttu-id="49b9f-112">Compatibilidade de aplicativos e padrões da Web</span><span class="sxs-lookup"><span data-stu-id="49b9f-112">Web Standards and Application Compatibility</span></span>](web-standards-and-application-compatibility.md)                                                       | <span data-ttu-id="49b9f-113">Fornece informações básicas sobre por que os padrões da Web são importantes.</span><span class="sxs-lookup"><span data-stu-id="49b9f-113">Provides background about why web standards are important.</span></span>                                |
| [<span data-ttu-id="49b9f-114">Atualizações de design que afetam a compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="49b9f-114">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)                           | <span data-ttu-id="49b9f-115">Fornece informações de tópicas sobre atualizações de design que afetam a compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="49b9f-115">Provides topical information about design updates that impact compatibility.</span></span>              |
| [<span data-ttu-id="49b9f-116">Corrigindo problemas de compatibilidade em aplicativos Web e Complementos</span><span class="sxs-lookup"><span data-stu-id="49b9f-116">Fixing Compatibility Issues in Web Applications and Add-Ons</span></span>](remediating-web-applications-and-add-ons.md)                                          | <span data-ttu-id="49b9f-117">Oferece sugestões para abordar problemas de compatibilidade com Complementos e aplicativos Web.</span><span class="sxs-lookup"><span data-stu-id="49b9f-117">Offers suggestions for addressing compatibility issues with web applications and add-ons.</span></span> |
| [<span data-ttu-id="49b9f-118">Ferramentas para depuração de aplicativos Web e Complementos</span><span class="sxs-lookup"><span data-stu-id="49b9f-118">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)                                             | <span data-ttu-id="49b9f-119">Lista as ferramentas disponíveis para depuração de aplicativos Web e Complementos.</span><span class="sxs-lookup"><span data-stu-id="49b9f-119">Lists tools that are available for debugging web applications and add-ons.</span></span>                |
| [<span data-ttu-id="49b9f-120">Apêndice 1: alterações no navegador do Internet Explorer 6 para o Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="49b9f-120">Appendix 1: Internet Explorer 6 to Internet Explorer 8 browser changes</span></span>](appendix-1--internet-explorer-6-to-internet-explorer-8-browser-changes.md) | <span data-ttu-id="49b9f-121">Lista as alterações do Microsoft Internet Explorer 6 para o Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="49b9f-121">Lists changes from Microsoft Internet Explorer 6 to Internet Explorer 8.</span></span>                  |
| [<span data-ttu-id="49b9f-122">Apêndice 2: cenários de script de teste</span><span class="sxs-lookup"><span data-stu-id="49b9f-122">Appendix 2: Test Script Scenarios</span></span>](appendix-2--test-script-scenarios.md)                                                                           | <span data-ttu-id="49b9f-123">Lista os cenários recomendados para testar a compatibilidade dos sites.</span><span class="sxs-lookup"><span data-stu-id="49b9f-123">Lists recommended scenarios for testing sites for compatibility.</span></span>                          |



 

 

 



