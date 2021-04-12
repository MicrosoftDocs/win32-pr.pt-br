---
title: Verificação de automação da interface do usuário (UIA verificar)
description: A verificação de automação da interface do usuário (UIA Verify) é uma estrutura de teste para teste manual e automatizado da implementação de um controle ou do aplicativo da automação da interface do usuário da Microsoft.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Verificação da Automação da Interface do Usuário
- Verificação de UIA
- Implementação da automação da interface do usuário, teste
- testando a automação da interface do usuário
- Ferramentas de teste de UIA
- Ferramentas de teste de automação da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365649"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="4f2cf-109">Ferramentas de acessibilidade – verificação de automação da interface do usuário (UIA verificar)</span><span class="sxs-lookup"><span data-stu-id="4f2cf-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="4f2cf-110">A **verificação de automação da interface do usuário (UIA Verify)** é uma estrutura de teste para teste manual e automatizado da implementação de um controle ou do aplicativo da automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="4f2cf-111">A maioria das funcionalidades da estrutura de teste vem de uma DLL chamada WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="4f2cf-112">Essa DLL contém o código para testar a funcionalidade de automação da interface do usuário específica e também dá suporte ao registro em log dos resultados do teste.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="4f2cf-113">Você pode integrar seu aplicativo no código de teste e realizar verificações regulares, automatizadas ou comparações de testes de seus cenários de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="4f2cf-114">O **UIA Verify** é instalado com o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4f2cf-115">Ele está localizado na \\ pasta bin \\ < *version* > \\ <  > \\ UIAVerify do caminho de instalação do SDK (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="4f2cf-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="4f2cf-116">A **verificação de UIA** consiste em uma API chamada biblioteca de teste de automação da interface do usuário e uma interface GUI chamada **verificação da automação da interface do usuário** Visual.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="4f2cf-117">Eles são descritos nos tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="4f2cf-118">A **verificação de automação da interface do usuário** é uma ferramenta herdada.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="4f2cf-119">Em vez disso, recomendamos o uso de [informações de acessibilidade](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="4f2cf-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f2cf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f2cf-120">Requirements</span></span>

<span data-ttu-id="4f2cf-121">A automação da interface do usuário deve estar presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="4f2cf-122">Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="4f2cf-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="4f2cf-123">A **verificação de UIA** é instalada como parte do conjunto geral de ferramentas no SDK do Windows, ela não é distribuída como um download separado.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="4f2cf-124">O SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="4f2cf-125">Obtenha o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f2cf-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="4f2cf-126">(Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)</span><span class="sxs-lookup"><span data-stu-id="4f2cf-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="4f2cf-127">Para executar o **UIA Verify** como uma ferramenta Visual, localize VisualUIAVerifyNative.exe na \\ pasta bin \\ < *Platform* > \\ UIAVerify e execute-o (normalmente, você não precisa executar como administrador).</span><span class="sxs-lookup"><span data-stu-id="4f2cf-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="4f2cf-128">Para obter mais informações, consulte [Visual IU Automation Verify](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="4f2cf-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="4f2cf-129">Para usar as bibliotecas, consulte [biblioteca de teste de automação da interface do usuário](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="4f2cf-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f2cf-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f2cf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f2cf-131">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="4f2cf-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="4f2cf-132">Inspecionar</span><span class="sxs-lookup"><span data-stu-id="4f2cf-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="4f2cf-133">Ferramentas de teste</span><span class="sxs-lookup"><span data-stu-id="4f2cf-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="4f2cf-134">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="4f2cf-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




