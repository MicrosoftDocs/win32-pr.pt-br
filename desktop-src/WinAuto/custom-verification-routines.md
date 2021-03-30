---
title: Rotinas de verificação personalizadas
description: Esta seção descreve como criar uma rotina de verificação personalizada para a ferramenta AccChecker (verificador de acessibilidade da interface do usuário).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916054"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="fa6f5-103">Rotinas de verificação personalizadas</span><span class="sxs-lookup"><span data-stu-id="fa6f5-103">Custom Verification Routines</span></span>

<span data-ttu-id="fa6f5-104">Esta seção descreve como criar uma rotina de verificação personalizada para a ferramenta AccChecker (verificador de acessibilidade da interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="fa6f5-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="fa6f5-105">Criando uma verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="fa6f5-106">Exemplo de verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="fa6f5-107">Usando uma verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="fa6f5-108">A GUI (interface gráfica do usuário) do AccChecker</span><span class="sxs-lookup"><span data-stu-id="fa6f5-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="fa6f5-109">Automação do AccChecker</span><span class="sxs-lookup"><span data-stu-id="fa6f5-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="fa6f5-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa6f5-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="fa6f5-111">O AccChecker (verificador de acessibilidade da interface do usuário) é uma ferramenta de teste de acessibilidade projetada para verificar a implementação do Microsoft Acessibilidade Ativa (MSAA) em uma interface do usuário do aplicativo ou controle.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="fa6f5-112">Problemas de acessibilidade de alto impacto que podem ser expostos pela implementação de MSAA são testados com um conjunto de rotinas de verificação automatizadas internas.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="fa6f5-113">Essas rotinas de verificação nativa podem ser aumentadas com rotinas personalizadas usando a plataforma AccChecker extensível.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="fa6f5-114">Criando uma verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-114">Creating a Custom Verification</span></span>

<span data-ttu-id="fa6f5-115">Uma verificação personalizada é criada como uma biblioteca de classes (DLL) que implementa uma única interface ( `IVerificationRoutine` ) que contém um membro ( `Execute` ):</span><span class="sxs-lookup"><span data-stu-id="fa6f5-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="fa6f5-116">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="fa6f5-116">**Parameters**</span></span>

<span data-ttu-id="fa6f5-117">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fa6f5-117">*hwnd*</span></span>

<span data-ttu-id="fa6f5-118">Tipo: **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="fa6f5-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="fa6f5-119">O HWND do elemento que está sendo verificado.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="fa6f5-120">*digita*</span><span class="sxs-lookup"><span data-stu-id="fa6f5-120">*logger*</span></span>

<span data-ttu-id="fa6f5-121">Tipo: **AccCheck. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="fa6f5-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="fa6f5-122">O método de log selecionado.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-122">The selected logging method.</span></span> <span data-ttu-id="fa6f5-123">Os tipos possíveis incluem **AccumulatingLogger** (usado pelo AccChecker para armazenar em cache todas as entradas de log até que as verificações sejam concluídas), **ConsoleLogger**, **TextFileLogger** e **XMLSerializingLogger**.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="fa6f5-124">*AllowUI*</span><span class="sxs-lookup"><span data-stu-id="fa6f5-124">*AllowUI*</span></span>

<span data-ttu-id="fa6f5-125">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="fa6f5-125">Type: **bool**</span></span>

<span data-ttu-id="fa6f5-126">Indica se a rotina de verificação exibe a interface do usuário que está testando.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="fa6f5-127">Geralmente definido como falso em cenários de teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="fa6f5-128">*gráficos*</span><span class="sxs-lookup"><span data-stu-id="fa6f5-128">*graphics*</span></span>

<span data-ttu-id="fa6f5-129">Tipo: **AccCheck. GraphicsHelper**</span><span class="sxs-lookup"><span data-stu-id="fa6f5-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="fa6f5-130">Usado para capturas de tela e outras visualizações no AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="fa6f5-131">Exemplo de verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-131">Sample Custom Verification</span></span>

<span data-ttu-id="fa6f5-132">O exemplo a seguir é uma verificação personalizada em C# que executa uma verificação de profundidade de árvore de elementos simples.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="fa6f5-133">Um erro será registrado se a árvore de elementos for maior que 50 níveis de profundidade, um aviso será registrado se a árvore de elementos for de 20 a 50 níveis de profundidade e uma mensagem informativa será registrada de outra forma.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="fa6f5-134">Uma solução Microsoft Visual Studio que contém o código de exemplo de verificação está incluída na documentação da ajuda.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="fa6f5-135">Os arquivos estão localizados no caminho de instalação do AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="fa6f5-136">Usando uma verificação personalizada</span><span class="sxs-lookup"><span data-stu-id="fa6f5-136">Using a Custom Verification</span></span>

<span data-ttu-id="fa6f5-137">Esta seção descreve como incorporar uma verificação personalizada em cenários de teste do AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="fa6f5-138">A GUI (interface gráfica do usuário) do AccChecker</span><span class="sxs-lookup"><span data-stu-id="fa6f5-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="fa6f5-139">Para incluir uma rotina de verificação personalizada no aplicativo AccChecker, basta clicar em abrir DLL no menu arquivo e localizar a DLL para a rotina.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="fa6f5-140">A rotina personalizada será adicionada à parte inferior da lista de verificações no painel Selecionar rotinas de verificação.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="fa6f5-141">A captura de tela a seguir mostra a verificação personalizada de profundidade da árvore de verificação de exemplo adicionada a AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![exemplo de rotina de verificação personalizada de profundidade da árvore de verificação adicionada à interface do usuário do amaccchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="fa6f5-143">Se os valores de atributo de verificação não forem especificados na rotina de verificação personalizada, a verificação ainda será carregada em AccChecker, mesmo que não apareça na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="fa6f5-144">Como não é exibido na interface do usuário, ele não pode ser desmarcado e excluído das execuções de verificação subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="fa6f5-145">Automação do AccChecker</span><span class="sxs-lookup"><span data-stu-id="fa6f5-145">AccChecker Automation</span></span>

<span data-ttu-id="fa6f5-146">Incorporar uma rotina de verificação personalizada em uma estrutura AccChecker automatizada é tão simples quanto adicionar a DLL de verificação e habilitar as rotinas de verificação desejadas.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="fa6f5-147">O trecho de código a seguir demonstra como usar a API AccChecker para testar a funcionalidade de tabulação no aplicativo do painel de controle do firewall do Windows.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Uma solução Microsoft Visual Studio 2008 que contém o código de exemplo de verificação está incluída na documentação da ajuda. <span data-ttu-id="fa6f5-149">Os arquivos estão localizados no caminho de instalação do AccChecker.</span><span class="sxs-lookup"><span data-stu-id="fa6f5-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fa6f5-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa6f5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa6f5-151">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="fa6f5-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




