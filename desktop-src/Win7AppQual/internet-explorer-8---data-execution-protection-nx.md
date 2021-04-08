---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-proteção de execução de dados/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf23ba40be518e3d4c1421012e6b46fdb7b5e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828817"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="7aae0-103">Internet Explorer 8-proteção de execução de dados/NX</span><span class="sxs-lookup"><span data-stu-id="7aae0-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7aae0-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="7aae0-104">Affected Platforms</span></span>

 <span data-ttu-id="7aae0-105">**Clientes** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="7aae0-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="7aae0-106">**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7aae0-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="7aae0-107">O Internet Explorer 8 habilitará a proteção DEP/NX quando for executado em um sistema operacional com as service pack mais recentes.</span><span class="sxs-lookup"><span data-stu-id="7aae0-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="7aae0-108">O Windows XP SP3, o Windows Server 2003 SP3, o Windows Vista SP1 e o Windows Server 2008 têm o DEP/NX habilitado por padrão no Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="7aae0-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="7aae0-109">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="7aae0-109">Feature Impact</span></span>

<span data-ttu-id="7aae0-110">**Severidade** -média</span><span class="sxs-lookup"><span data-stu-id="7aae0-110">**Severity** - Medium</span></span>  
<span data-ttu-id="7aae0-111">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="7aae0-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="7aae0-112">Normalmente, qualquer aplicativo executado no Internet Explorer e não é compatível com o DEP/NX falhará na inicialização e não funcionará.</span><span class="sxs-lookup"><span data-stu-id="7aae0-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="7aae0-113">O Internet Explorer poderá falhar na inicialização se os complementos não compatíveis com o DEP/NX estiverem instalados.</span><span class="sxs-lookup"><span data-stu-id="7aae0-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="7aae0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aae0-114">Description</span></span>

<span data-ttu-id="7aae0-115">O DEP/NX é um recurso de segurança que ajuda a reduzir vulnerabilidades relacionadas à memória.</span><span class="sxs-lookup"><span data-stu-id="7aae0-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="7aae0-116">A partir do Internet Explorer 8, todos os processos do Internet Explorer habilitam o recurso DEP/NX por padrão.</span><span class="sxs-lookup"><span data-stu-id="7aae0-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7aae0-117">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="7aae0-117">Manifestation of Impact</span></span>

<span data-ttu-id="7aae0-118">O kernel do Windows monitora a execução de um programa.</span><span class="sxs-lookup"><span data-stu-id="7aae0-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="7aae0-119">Se o kernel detectar uma tentativa de executar o código de uma página de memória que não esteja marcada como executável, o kernel interromperá a execução do programa, resultando em uma "falha".</span><span class="sxs-lookup"><span data-stu-id="7aae0-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="7aae0-120">Essa é uma medida de segurança para ajudar a garantir que vulnerabilidades relacionadas à memória (por exemplo, estouros de buffer) no aplicativo não possam ser exploradas para executar código arbitrário.</span><span class="sxs-lookup"><span data-stu-id="7aae0-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="7aae0-121">Mitigação de End-User</span><span class="sxs-lookup"><span data-stu-id="7aae0-121">End-User Mitigation</span></span>

-   <span data-ttu-id="7aae0-122">Instale uma versão mais recente do complemento ou da estrutura compatível com o DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7aae0-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="7aae0-123">Execute o Internet Explorer com privilégios elevados como administrador e, em seguida, desabilite o DEP/NX usando a caixa de seleção **habilitar proteção de memória para ajudar a atenuar os ataques online** na guia Avançado **Opções da Internet**  /   .</span><span class="sxs-lookup"><span data-stu-id="7aae0-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="7aae0-124">Solução de desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="7aae0-124">Developer Solution</span></span>

<span data-ttu-id="7aae0-125">Compile aplicativos usando as versões mais recentes das estruturas compatíveis com o DEP.</span><span class="sxs-lookup"><span data-stu-id="7aae0-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="7aae0-126">Aproveitando os recursos do recurso</span><span class="sxs-lookup"><span data-stu-id="7aae0-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="7aae0-127">Use a opção de vinculador/NXCOMPAT para indicar a compatibilidade com DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7aae0-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="7aae0-128">Opte pelo seu código em outras defesas disponíveis, como o conjunto de defesa (/GS), o/SafeSEH (tratamento de exceção segura) e a ASLR (/DynamicBase)</span><span class="sxs-lookup"><span data-stu-id="7aae0-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="7aae0-129">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="7aae0-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="7aae0-130">Teste seu código com o DEP/NX habilitado usando a última versão do Internet Explorer lançada no Windows Vista SP1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7aae0-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="7aae0-131">Teste com o Internet Explorer 7 no Windows Vista depois de habilitar a opção DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7aae0-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="7aae0-132">Para habilitar o DEP/NX para Internet Explorer 7, execute o Internet Explorer como administrador e, em seguida, defina a caixa de seleção apropriada na guia ferramentas > opções da Internet > avançado.</span><span class="sxs-lookup"><span data-stu-id="7aae0-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="7aae0-133">Execute a ferramenta de teste de compatibilidade do Internet Explorer (IECTT), fornecida com o kit de ferramentas de compatibilidade de aplicativos (ACT) para localizar possíveis problemas devido às alterações de DEP/NX.</span><span class="sxs-lookup"><span data-stu-id="7aae0-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7aae0-134">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="7aae0-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="7aae0-135">Internet Explorer 8 parte I: proteção de memória DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7aae0-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="7aae0-136">Prevenção de execução de dados</span><span class="sxs-lookup"><span data-stu-id="7aae0-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="7aae0-137">Novas APIs NX adicionadas ao Windows Vista SP1, Windows XP SP3 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7aae0-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="7aae0-138">Download do kit de ferramentas de compatibilidade de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7aae0-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="7aae0-139">[Problemas conhecidos do recurso de segurança do Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="7aae0-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
