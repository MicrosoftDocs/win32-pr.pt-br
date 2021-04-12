---
title: O que há de novo no WER
description: Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.
ms.assetid: 6cdd6c64-ba67-40dc-9942-0371320f1881
keywords:
- Relatório de erros do Windows Relatório de Erros do Windows, o que há de novo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526776de3c5f88400e7cfae7ed9b9717318c223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293897"
---
# <a name="whats-new-in-wer"></a><span data-ttu-id="e75e5-104">O que há de novo no WER</span><span class="sxs-lookup"><span data-stu-id="e75e5-104">What's New in WER</span></span>

<span data-ttu-id="e75e5-105">Esta página resume os novos recursos do Relatório de Erros do Windows (WER) para cada versão.</span><span class="sxs-lookup"><span data-stu-id="e75e5-105">This page summarizes the new features of Windows Error Reporting (WER) for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="e75e5-106">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e75e5-106">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="e75e5-107">A lista a seguir resume os novos recursos do WER para o Windows 7 e o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e75e5-107">The following list summarizes the new WER features for Windows 7 and Windows Server 2008 R2.</span></span>

-   <span data-ttu-id="e75e5-108">Adiciona a capacidade de gerar uma exceção que ignora todos os manipuladores de exceção, encerrando o aplicativo imediatamente e invocando Relatório de Erros do Windows.</span><span class="sxs-lookup"><span data-stu-id="e75e5-108">Adds the ability to raise an exception that bypasses all exception handlers thus terminating the application immediately and invoking Windows Error Reporting.</span></span> <span data-ttu-id="e75e5-109">Para obter detalhes, consulte a função [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e75e5-109">For details, see the [**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85)) function.</span></span>
-   <span data-ttu-id="e75e5-110">Adiciona a capacidade de registrar um manipulador de exceção fora do processo que o WER chama quando ocorre uma falha para coletar o nome do evento, os parâmetros de relatório e as opções de inicialização de depuração.</span><span class="sxs-lookup"><span data-stu-id="e75e5-110">Adds the ability to register an out-of-process exception handler that WER calls when a crash occurs to collect the event name, reporting parameters, and debug launching options.</span></span> <span data-ttu-id="e75e5-111">Para obter detalhes, consulte a função [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) .</span><span class="sxs-lookup"><span data-stu-id="e75e5-111">For details, see the [**WerRegisterRuntimeExceptionModule**](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule) function.</span></span>

<span data-ttu-id="e75e5-112">Funções que foram adicionadas:</span><span class="sxs-lookup"><span data-stu-id="e75e5-112">Functions that were added:</span></span>

-   [<span data-ttu-id="e75e5-113">**OutOfProcessExceptionEventCallback**</span><span class="sxs-lookup"><span data-stu-id="e75e5-113">**OutOfProcessExceptionEventCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event)
-   [<span data-ttu-id="e75e5-114">**OutOfProcessExceptionEventSignatureCallback**</span><span class="sxs-lookup"><span data-stu-id="e75e5-114">**OutOfProcessExceptionEventSignatureCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_event_signature)
-   [<span data-ttu-id="e75e5-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span><span class="sxs-lookup"><span data-stu-id="e75e5-115">**OutOfProcessExceptionEventDebuggerLaunchCallback**</span></span>](/windows/desktop/api/Werapi/nc-werapi-pfn_wer_runtime_exception_debugger_launch)
-   <span data-ttu-id="e75e5-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e75e5-116">[**RaiseFailFastException**](/previous-versions/dd408166(v=vs.85))</span></span>
-   [<span data-ttu-id="e75e5-117">**WerRegisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="e75e5-117">**WerRegisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werregisterruntimeexceptionmodule)
-   [<span data-ttu-id="e75e5-118">**WerUnregisterRuntimeExceptionModule**</span><span class="sxs-lookup"><span data-stu-id="e75e5-118">**WerUnregisterRuntimeExceptionModule**</span></span>](/windows/desktop/api/Werapi/nf-werapi-werunregisterruntimeexceptionmodule)

<span data-ttu-id="e75e5-119">Estruturas que foram adicionadas:</span><span class="sxs-lookup"><span data-stu-id="e75e5-119">Structures that were added:</span></span>

-   [<span data-ttu-id="e75e5-120">**informações de exceção de tempo de execução do WER \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e75e5-120">**WER\_RUNTIME\_EXCEPTION\_INFORMATION**</span></span>](/windows/desktop/api/Werapi/ns-werapi-wer_runtime_exception_information)

## <a name="windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="e75e5-121">Windows Server 2008 e Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="e75e5-121">Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="e75e5-122">A lista a seguir resume os novos recursos do WER para Windows Server 2008 e Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e75e5-122">The following list summarizes the new features of WER for Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

-   <span data-ttu-id="e75e5-123">O WER pode ser configurado para que os despejos completos do modo de usuário sejam coletados e armazenados localmente após a falha de um aplicativo de modo de usuário (os aplicativos que realizam seus próprios relatórios de falhas personalizados, incluindo aplicativos .NET, não têm suporte).</span><span class="sxs-lookup"><span data-stu-id="e75e5-123">WER can be configured so that full user-mode dumps are collected and stored locally after a user-mode application crashes (applications that do their own custom crash reporting, including .NET applications are not supported).</span></span> <span data-ttu-id="e75e5-124">Para obter mais informações, consulte [coletando despejos de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="e75e5-124">For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

## <a name="windows-vista"></a><span data-ttu-id="e75e5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e75e5-125">Windows Vista</span></span>

<span data-ttu-id="e75e5-126">A lista a seguir resume os novos recursos do Relatório de Erros do Windows (WER) para o Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="e75e5-126">The following list summarizes the new features of Windows Error Reporting (WER) for Windows Vista:</span></span>

-   <span data-ttu-id="e75e5-127">O WER foi estendido além do monitoramento de falhas e de processos sem resposta.</span><span class="sxs-lookup"><span data-stu-id="e75e5-127">WER has been extended beyond monitoring crashes and unresponsive processes.</span></span> <span data-ttu-id="e75e5-128">O WER inclui suporte para muitos novos tipos de eventos não críticos, como problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e75e5-128">WER includes support for many new types of non-critical events, such as performance issues.</span></span> <span data-ttu-id="e75e5-129">Isso permite que os desenvolvedores aprendam mais sobre as experiências que seus clientes têm com os aplicativos que desenvolveram.</span><span class="sxs-lookup"><span data-stu-id="e75e5-129">This enables developers to learn more about the experiences their customers have with the applications they have developed.</span></span>
-   <span data-ttu-id="e75e5-130">Novas funções oferecem aos desenvolvedores a flexibilidade de criar, personalizar e enviar relatórios de problemas.</span><span class="sxs-lookup"><span data-stu-id="e75e5-130">New functions give developers the flexibility in creating, customizing, and submitting problem reports.</span></span> <span data-ttu-id="e75e5-131">Para obter mais informações, consulte [funções do WER](wer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e75e5-131">For more information, see [WER Functions](wer-functions.md).</span></span>
-   <span data-ttu-id="e75e5-132">O [Windows Quality Online Services](https://www.microsoft.com/?ref=go) aprimorado fornece aos desenvolvedores acesso às informações do problema que os clientes estão enviando para seus aplicativos e um mecanismo para fornecer soluções a esses clientes.</span><span class="sxs-lookup"><span data-stu-id="e75e5-132">The improved [Windows Quality Online Services](https://www.microsoft.com/?ref=go) provides developers with access to the problem information that customers are submitting for their applications, and a mechanism to deliver solutions to these customers.</span></span>
-   <span data-ttu-id="e75e5-133">As funções introduzidas pelo Gerenciador de [recuperação e reinicialização](/windows/desktop/Recovery/application-recovery-and-restart-portal) e [reinicialização](/windows/desktop/RstMgr/restart-manager-portal) do aplicativo permitem que os aplicativos recuperem automaticamente as informações e reiniciem em caso de falha crítica.</span><span class="sxs-lookup"><span data-stu-id="e75e5-133">The functions introduced by [Application Recovery and Restart](/windows/desktop/Recovery/application-recovery-and-restart-portal) and [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) enable applications to automatically recover information and restart in the event of a critical failure.</span></span> <span data-ttu-id="e75e5-134">Os desenvolvedores podem usar esses recursos em seus aplicativos para melhorar significativamente a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="e75e5-134">Developers can use these features in their applications to significantly improve their user experience.</span></span>
-   <span data-ttu-id="e75e5-135">**Relatórios de problemas e soluções no Windows Vista ou na central de ações no Windows 7** é o local central para os usuários interagirem com o wer.</span><span class="sxs-lookup"><span data-stu-id="e75e5-135">**Problem Reports and Solutions on Windows Vista or the Action Center on Windows 7** is the central location for users to interact with WER.</span></span> <span data-ttu-id="e75e5-136">Os usuários podem verificar se há novas soluções, gerenciar o histórico de relatórios, exibir os detalhes de um relatório de problemas e gerenciar configurações de relatórios, incluindo a habilitação do WER para verificar se há soluções automaticamente, sem interromper o usuário.</span><span class="sxs-lookup"><span data-stu-id="e75e5-136">Users can check for new solutions, manage their reporting history, view the details of a problem report, and manage reporting settings including enabling WER to check for solutions automatically without interrupting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e75e5-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e75e5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e75e5-138">Relatório de Erros do Windows</span><span class="sxs-lookup"><span data-stu-id="e75e5-138">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 