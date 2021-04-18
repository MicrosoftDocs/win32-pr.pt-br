---
title: Ferramentas de acessibilidade – AccChecker (verificador de acessibilidade da interface do usuário)
description: Descreve o AccChecker (verificador de acessibilidade da interface do usuário), uma ferramenta para testar a automação da interface do usuário do aplicativo ou a implementação do Microsoft Acessibilidade Ativa (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Implementação da automação da interface do usuário, teste
- Implementação de UIA, teste
- Implementação do Microsoft Acessibilidade Ativa, testes
- Implementação de MSAA, teste
- testando a automação da interface do usuário
- testando UIA
- testando o Microsoft Acessibilidade Ativa
- testando a MSAA
- Ferramentas de teste de UIA
- Ferramentas de teste de automação da interface do usuário
- Ferramentas de teste de MSAA
- Ferramentas de teste do Microsoft Acessibilidade Ativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105810780"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="4648a-117">Ferramentas de acessibilidade – AccChecker (verificador de acessibilidade da interface do usuário)</span><span class="sxs-lookup"><span data-stu-id="4648a-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="4648a-118">**AccChecker** (verificador de acessibilidade da interface do usuário) verifica se os principais requisitos de acessibilidade da interface do usuário são atendidos no design e na implementação da UIA (automação da interface do usuário) ou Microsoft acessibilidade ativa (MSAA), independentemente da estrutura subjacente da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4648a-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="4648a-119">O **AccChecker** também inclui um conjunto de verificações de acessibilidade da Web.</span><span class="sxs-lookup"><span data-stu-id="4648a-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="4648a-120">O **AccChecker** fornece os seguintes níveis de funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="4648a-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="4648a-121">Um aplicativo de GUI do Windows que dá suporte a testes manuais, registro de mensagens e geração de supressão.</span><span class="sxs-lookup"><span data-stu-id="4648a-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="4648a-122">Uma API para uso em estruturas de teste automatizadas.</span><span class="sxs-lookup"><span data-stu-id="4648a-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="4648a-123">Um aplicativo de console que dá suporte a automaçãos de teste não gerenciadas para cenários em que a API gerenciada **AccChecker** não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="4648a-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="4648a-124">Todos os níveis de funcionalidade do **AccChecker** fornecem rotinas para verificar o acesso programático ao Microsoft acessibilidade ativa, geração de eventos programático, layout de controle e navegação por teclado.</span><span class="sxs-lookup"><span data-stu-id="4648a-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="4648a-125">O **AccChecker** também fornece um serviço básico de transcrição de leitor de tela.</span><span class="sxs-lookup"><span data-stu-id="4648a-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="4648a-126">O **AccChecker** é instalado com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="4648a-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4648a-127">Ele está localizado na \\ pasta bin \\ < *version* > \\ <  > \\ AccChecker do caminho de instalação do SDK.</span><span class="sxs-lookup"><span data-stu-id="4648a-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="4648a-128">**AccChecker** é uma ferramenta herdada.</span><span class="sxs-lookup"><span data-stu-id="4648a-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="4648a-129">Em vez disso, recomendamos o uso de [informações de acessibilidade](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="4648a-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="4648a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4648a-130">Requirements</span></span>

<span data-ttu-id="4648a-131">Requer o .NET Framework 2,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4648a-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="4648a-132">O **AccChecker** pode ser usado para examinar dados de acessibilidade em sistemas que não têm a automação da interface do usuário da Microsoft, mas só pode examinar as propriedades do Microsoft acessibilidade ativa.</span><span class="sxs-lookup"><span data-stu-id="4648a-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="4648a-133">Para examinar a automação da interface do usuário, a automação da interface do usuário deve estar presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="4648a-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="4648a-134">Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="4648a-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="4648a-135">O **AccChecker** é instalado como parte do conjunto geral de ferramentas no SDK do Windows, ele não é distribuído como um download de exe separado.</span><span class="sxs-lookup"><span data-stu-id="4648a-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="4648a-136">O SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="4648a-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="4648a-137">Obtenha o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="4648a-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="4648a-138">(Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)</span><span class="sxs-lookup"><span data-stu-id="4648a-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4648a-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4648a-139">Related topics</span></span>

- [<span data-ttu-id="4648a-140">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="4648a-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="4648a-141">Inspecionar</span><span class="sxs-lookup"><span data-stu-id="4648a-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="4648a-142">Ferramentas de teste</span><span class="sxs-lookup"><span data-stu-id="4648a-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="4648a-143">Verificação da Automação da Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="4648a-143">UI Automation Verify</span></span>](ui-automation-verify.md)
