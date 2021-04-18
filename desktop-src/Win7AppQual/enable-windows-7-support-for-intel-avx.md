---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Habilitar o suporte do Windows 7 para Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781625"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="72583-103">Habilitar o suporte do Windows 7 para Intel AVX</span><span class="sxs-lookup"><span data-stu-id="72583-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="72583-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="72583-104">Affected Platforms</span></span>

 <span data-ttu-id="72583-105">**Clientes** -Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="72583-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="72583-106">**Servidores** -Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="72583-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="72583-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="72583-107">Feature Impact</span></span>

 <span data-ttu-id="72583-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="72583-108">**Severity** - Low</span></span>  
<span data-ttu-id="72583-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="72583-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="72583-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="72583-110">Description</span></span>

<span data-ttu-id="72583-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="72583-111">Intel<sup>?</sup></span></span> <span data-ttu-id="72583-112">Extensões de vetor avançadas (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="72583-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="72583-113">é uma extensão de vetor de ponto flutuante de 256-bit SIMD da arquitetura Intel.</span><span class="sxs-lookup"><span data-stu-id="72583-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="72583-114">Ele inclui extensões para os conjuntos de instruções e de registro.</span><span class="sxs-lookup"><span data-stu-id="72583-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="72583-115">A Microsoft desenvolveu alguns aprimoramentos de API, como o XState functions, que permitem que os aplicativos acessem e manipulem informações e estado do recurso do processador estendido, incluindo AVX.</span><span class="sxs-lookup"><span data-stu-id="72583-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="72583-116">Cenários de uso</span><span class="sxs-lookup"><span data-stu-id="72583-116">Usage Scenarios</span></span>

<span data-ttu-id="72583-117">Há três níveis gerais de impacto potencial.</span><span class="sxs-lookup"><span data-stu-id="72583-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="72583-118">**Nível 1:** Os aplicativos que não usam o Intel AVX diretamente não verão nenhum impacto sobre sua funcionalidade, mesmo que eles chamem em bibliotecas ou usem compiladores que usam indiretamente ou gerem extensões Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="72583-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="72583-119">Isso representa, de longe, a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="72583-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="72583-120">**Nível 2:** Os aplicativos avançados que usam explicitamente o conjunto de instruções Intel AVX poderão acessar e alterar o conteúdo do registro do AVX quando uma exceção de hardware for gerada.</span><span class="sxs-lookup"><span data-stu-id="72583-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="72583-121">Um número muito pequeno de aplicativos se enquadraria nessa categoria, pois implica um conhecimento profundo do fluxo de instrução em execução no momento da exceção, como aplicativos com seções escritas em linguagem de assembly ou aqueles que geram código de máquina em tempo de execução (por exemplo, tempos de execução de código gerenciado com compilação just-in-time).</span><span class="sxs-lookup"><span data-stu-id="72583-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="72583-122">**Nível 3:** Os aplicativos do depurador poderão acessar e manipular o estado AVX no aplicativo que está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="72583-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="72583-123">Como aproveitar os recursos de recursos</span><span class="sxs-lookup"><span data-stu-id="72583-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="72583-124">**Nível 1:** Nenhuma ação é necessária para que os aplicativos usem o Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="72583-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="72583-125">**Nível 2:** Os aplicativos nessa categoria têm a opção de acessar e manipular o estado AVX no momento da exceção de dentro de seus filtros de exceção.</span><span class="sxs-lookup"><span data-stu-id="72583-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="72583-126">Depois de obter o contexto do processador base via GetExceptionInformation, os filtros devem:</span><span class="sxs-lookup"><span data-stu-id="72583-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="72583-127">**1.** Verifique o valor do sinalizador **\_ XSTATE do contexto** .</span><span class="sxs-lookup"><span data-stu-id="72583-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="72583-128">Esse sinalizador indica a presença de pelo menos um recurso XState no contexto.</span><span class="sxs-lookup"><span data-stu-id="72583-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="72583-129">**2.** se esse for o caso, chame **GetXStateFeaturesMask** e teste o valor do sinalizador **XSTATE \_ AVX** na máscara retornada.</span><span class="sxs-lookup"><span data-stu-id="72583-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="72583-130">Isso indica a presença do estado AVX no contexto.</span><span class="sxs-lookup"><span data-stu-id="72583-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="72583-131">**3.** chame **LocateXStateFeature** para recuperar o local real onde o estado AVX está armazenado.</span><span class="sxs-lookup"><span data-stu-id="72583-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="72583-132">**Nível 3:** Não é necessário atualizar os aplicativos de depurador existentes, a menos que desejem acessar os registros do Intel AVX:</span><span class="sxs-lookup"><span data-stu-id="72583-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="72583-133">**1.** para determinar se o AVX está habilitado, o depurador deve usar:</span><span class="sxs-lookup"><span data-stu-id="72583-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="72583-134">GetEnabledXStateFeatures para obter uma máscara de recursos de XState habilitados em processadores x86 ou x64 para determinar quais recursos estão presentes e habilitados no sistema antes de usar um recurso de processador XState ou tentar manipular os contextos XState</span><span class="sxs-lookup"><span data-stu-id="72583-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="72583-135">**2.** se AVX estiver presente e você desejar recuperar e manipular o estado AVX do aplicativo que está sendo depurado (por exemplo, GetThreadContext e SetThreadContext), o depurador deverá usar:</span><span class="sxs-lookup"><span data-stu-id="72583-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="72583-136">Função InitializeContext para inicializar uma estrutura de contexto dentro de um buffer com o tamanho e o alinhamento necessários</span><span class="sxs-lookup"><span data-stu-id="72583-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="72583-137">Função CopyContext para copiar uma estrutura de contexto de origem (incluindo qualquer XState) em uma estrutura de contexto de destino inicializada</span><span class="sxs-lookup"><span data-stu-id="72583-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="72583-138">**3.** para testar, definir e localizar o estado AVX dentro de um contexto de processador, o depurador deve usar:</span><span class="sxs-lookup"><span data-stu-id="72583-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="72583-139">LocateXStateFeature para recuperar um ponteiro para o estado do processador para um recurso de XState individual dentro de uma estrutura de contexto</span><span class="sxs-lookup"><span data-stu-id="72583-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="72583-140">GetXStateFeaturesMask para retornar a máscara do conjunto de recursos do XState em uma estrutura de contexto</span><span class="sxs-lookup"><span data-stu-id="72583-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="72583-141">SetXStateFeaturesMask para definir a máscara do conjunto de recursos do XState em uma estrutura de contexto</span><span class="sxs-lookup"><span data-stu-id="72583-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="72583-142">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="72583-142">Links to Other Resources</span></span>

-   <span data-ttu-id="72583-143">Para obter informações sobre as funções XState no SDK do Windows, consulte [Debugging Functions](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="72583-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="72583-144">Para obter uma visão geral das instruções e dos recursos do Intel AVX, consulte [Intel AVX: novas fronteiras em melhorias de desempenho e eficiência energética](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="72583-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
