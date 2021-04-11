---
title: Diretrizes gerais de portabilidade
description: Portar aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que portar aplicativos de 16 bits para o Windows de 32 bits. No entanto, a mudança ficará mais tranqüila com um planejamento cuidadoso. Veja a seguir algumas diretrizes gerais.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- portando aplicativos de 32 bits para programação do Windows de 64 bits Windows de 64 bits
- Guia de programação do Windows de 64 bits – programação do Windows de 64 bits, diretrizes de portabilidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104172414"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="7b867-107">Diretrizes gerais de portabilidade</span><span class="sxs-lookup"><span data-stu-id="7b867-107">General Porting Guidelines</span></span>

<span data-ttu-id="7b867-108">Portar aplicativos de 32 bits para o Microsoft Windows de 64 bits será mais fácil do que portar aplicativos de 16 bits para o Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="7b867-109">No entanto, a mudança ficará mais tranqüila com um planejamento cuidadoso.</span><span class="sxs-lookup"><span data-stu-id="7b867-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="7b867-110">Veja a seguir algumas diretrizes gerais.</span><span class="sxs-lookup"><span data-stu-id="7b867-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="7b867-111">Planejamento</span><span class="sxs-lookup"><span data-stu-id="7b867-111">Planning</span></span>

-   <span data-ttu-id="7b867-112">Determine a magnitude do esforço necessário para a porta.</span><span class="sxs-lookup"><span data-stu-id="7b867-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="7b867-113">Avalie a quantidade de trabalho envolvida identificando os seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="7b867-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="7b867-114">Problema 32-código de bit.</span><span class="sxs-lookup"><span data-stu-id="7b867-114">Problem 32-bit code.</span></span> <span data-ttu-id="7b867-115">Compile o código de 32 bits com o compilador de 64 bits e examine a extensão dos erros e avisos.</span><span class="sxs-lookup"><span data-stu-id="7b867-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="7b867-116">Componentes compartilhados ou dependências.</span><span class="sxs-lookup"><span data-stu-id="7b867-116">Shared components or dependencies.</span></span> <span data-ttu-id="7b867-117">Determine quais componentes em seu aplicativo se originam de outras equipes e se essas equipes planejam desenvolver versões de 64 bits de seu código.</span><span class="sxs-lookup"><span data-stu-id="7b867-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="7b867-118">Código herdado ou assembly.</span><span class="sxs-lookup"><span data-stu-id="7b867-118">Legacy or assembly code.</span></span> <span data-ttu-id="7b867-119">aplicativos baseados no Windows de 16 bits não são executados em janelas de 64 bits e devem ser reescritos.</span><span class="sxs-lookup"><span data-stu-id="7b867-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="7b867-120">Embora o código do assembly x86 seja executado no WOW64, talvez você queira reescrever esse código para aproveitar a velocidade da arquitetura Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="7b867-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="7b867-121">Portar todo o aplicativo, não apenas partes dele.</span><span class="sxs-lookup"><span data-stu-id="7b867-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="7b867-122">Embora seja possível portar partes de um aplicativo ou limitar o código a 2G com/LARGEADDRESSAWARE: não, essa estratégia compensa o lucro de curto prazo para problemas de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7b867-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="7b867-123">/LARGEADDRESSAWARE: não é ignorado para um binário ARM64.</span><span class="sxs-lookup"><span data-stu-id="7b867-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="7b867-124">Localize substitutos para tecnologias que não serão portadas.</span><span class="sxs-lookup"><span data-stu-id="7b867-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="7b867-125">Algumas tecnologias, incluindo o DAO (objeto de acesso a dados) e o mecanismo de banco de dados do Jet Red, não serão portadas para o Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="7b867-126">Trate sua versão de 64 bits como uma versão de produto separada.</span><span class="sxs-lookup"><span data-stu-id="7b867-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="7b867-127">Embora seu produto de 64 bits possa compartilhar a mesma base de código que o de 32 bits, ele precisa de testes adicionais e pode ter outras considerações de versão.</span><span class="sxs-lookup"><span data-stu-id="7b867-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="7b867-128">Desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="7b867-128">Development</span></span>

-   <span data-ttu-id="7b867-129">Comece a desenvolver código em conformidade agora mesmo.</span><span class="sxs-lookup"><span data-stu-id="7b867-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="7b867-130">Os desenvolvedores podem começar a escrever código em conformidade usando os arquivos de cabeçalho mais recentes do Windows e os novos tipos de dados sem efeitos adversos no desenvolvimento de produtos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="7b867-131">Para obter mais informações, consulte [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="7b867-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="7b867-132">Verifique se seu código pode ser compilado para o Windows de 32 e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="7b867-133">O novo modelo de dados foi projetado para permitir que aplicativos de 32 e 64 bits sejam criados a partir de uma única base de código com poucas modificações.</span><span class="sxs-lookup"><span data-stu-id="7b867-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="7b867-134">As equipes de desenvolvimento SQL Server e Windows estão desenvolvendo versões de 32 e 64 bits de seus produtos na mesma base de código.</span><span class="sxs-lookup"><span data-stu-id="7b867-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="7b867-135">Use os novos recursos de otimização do compilador para obter o melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="7b867-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="7b867-136">A otimização de código para processadores Intel Itanium é mais importante do que era para o x86.</span><span class="sxs-lookup"><span data-stu-id="7b867-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="7b867-137">O compilador assume muitas das funções de otimização previamente tratadas pelo microprocessador.</span><span class="sxs-lookup"><span data-stu-id="7b867-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="7b867-138">Você pode maximizar o desempenho de um aplicativo de 64 bits usando dois novos recursos de otimização do compilador: *otimização guiada por perfil* e *otimização de programa completa*.</span><span class="sxs-lookup"><span data-stu-id="7b867-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="7b867-139">Os dois recursos resultam em tempos de compilação mais longos e exigem o desenvolvimento antecipado de bons cenários de teste.</span><span class="sxs-lookup"><span data-stu-id="7b867-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="7b867-140">A *otimização guiada por perfil* envolve um processo de compilação em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="7b867-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="7b867-141">Durante a primeira compilação, o código é instrumentado para capturar o comportamento de execução.</span><span class="sxs-lookup"><span data-stu-id="7b867-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="7b867-142">Essas informações são usadas durante a segunda compilação para guiar todos os recursos de otimização.</span><span class="sxs-lookup"><span data-stu-id="7b867-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="7b867-143">A *otimização completa do programa* analisa o código em todos os arquivos de aplicativo, não apenas um único.</span><span class="sxs-lookup"><span data-stu-id="7b867-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="7b867-144">Essa abordagem aumenta o desempenho de várias maneiras, incluindo a melhor linhagem, bem como a análise de efeito colateral e as convenções de chamada personalizadas aprimoradas.</span><span class="sxs-lookup"><span data-stu-id="7b867-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="7b867-145">Teste</span><span class="sxs-lookup"><span data-stu-id="7b867-145">Testing</span></span>

-   <span data-ttu-id="7b867-146">Determine se você testará o código de 64 ou 32 bits em execução no WOW64.</span><span class="sxs-lookup"><span data-stu-id="7b867-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="7b867-147">Alguns aplicativos incluem código de 64 bits nativo e código de 32 bits em execução no WOW64.</span><span class="sxs-lookup"><span data-stu-id="7b867-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="7b867-148">Investigue isso atentamente ao desenvolver um plano de teste e decida se suas ferramentas de teste devem ser de 64 bits, 32 bits ou uma combinação.</span><span class="sxs-lookup"><span data-stu-id="7b867-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="7b867-149">Muitas vezes, você precisará testar as versões de 64 e 32 bits do seu aplicativo no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="7b867-150">Teste os componentes de 32 bits usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="7b867-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="7b867-151">Primeiro, recompile seu código para 64 bits e teste.</span><span class="sxs-lookup"><span data-stu-id="7b867-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="7b867-152">Em segundo lugar, corrija os problemas, recompile em 32 bits e, em seguida, teste.</span><span class="sxs-lookup"><span data-stu-id="7b867-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="7b867-153">Terceiro, recompile para 64 bits e teste.</span><span class="sxs-lookup"><span data-stu-id="7b867-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="7b867-154">Testar componentes COM e RPC.</span><span class="sxs-lookup"><span data-stu-id="7b867-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="7b867-155">Certifique-se de que os componentes COM e RPC de 32 e 64 bits se comuniquem corretamente.</span><span class="sxs-lookup"><span data-stu-id="7b867-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="7b867-156">Você também pode precisar testar as comunicações com componentes de 16 bits em uma rede.</span><span class="sxs-lookup"><span data-stu-id="7b867-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="7b867-157">Teste sua versão de 32 bits em Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7b867-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="7b867-158">Os clientes podem continuar a usar aplicativos de 32 bits em janelas de 64 bits em que os problemas de desempenho e memória não são considerações importantes.</span><span class="sxs-lookup"><span data-stu-id="7b867-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="7b867-159">Teste configurações de memória diferentes.</span><span class="sxs-lookup"><span data-stu-id="7b867-159">Test different memory configurations.</span></span>

    <span data-ttu-id="7b867-160">A adição de grandes quantidades de memória no servidor às vezes expõe problemas despercebidos anteriormente no aplicativo ou no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7b867-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




