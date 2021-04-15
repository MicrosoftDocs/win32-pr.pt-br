---
title: Biblioteca de teste de automação da interface do usuário
description: A biblioteca de testes de automação da interface do usuário (biblioteca de teste UIA) é uma API que é chamada pelo aplicativo de driver em um cenário de teste automatizado.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104556462"
---
# <a name="ui-automation-test-library"></a><span data-ttu-id="60f29-103">Biblioteca de teste de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="60f29-103">UI Automation Test Library</span></span>

<span data-ttu-id="60f29-104">A biblioteca de testes de automação da interface do usuário (biblioteca de teste UIA) é uma API que é chamada pelo aplicativo de *Driver* em um cenário de teste automatizado.</span><span class="sxs-lookup"><span data-stu-id="60f29-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="60f29-105">O driver é o aplicativo que obtém um elemento Automation (objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) de um controle que requer verificação e o fornece à biblioteca de teste de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60f29-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="60f29-106">Em seguida, a biblioteca de testes verifica e valida a implementação da automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60f29-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="60f29-107">Para saber mais sobre automação da interface do usuário e elementos de automação, confira [conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60f29-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="60f29-108">Fluxo de trabalho da biblioteca de teste de automação da IU</span><span class="sxs-lookup"><span data-stu-id="60f29-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="60f29-109">Registro em log com a biblioteca de teste de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="60f29-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="60f29-110">Log XML</span><span class="sxs-lookup"><span data-stu-id="60f29-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="60f29-111">Log de console</span><span class="sxs-lookup"><span data-stu-id="60f29-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="60f29-112">Requisitos de código para registro em log</span><span class="sxs-lookup"><span data-stu-id="60f29-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="60f29-113">Exemplos de log</span><span class="sxs-lookup"><span data-stu-id="60f29-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="60f29-114">Fluxo de trabalho da biblioteca de teste de automação da IU</span><span class="sxs-lookup"><span data-stu-id="60f29-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="60f29-115">O diagrama a seguir mostra um fluxo de trabalho de teste que incorpora a biblioteca de teste de automação da interface do usuário usando um aplicativo de console como o driver.</span><span class="sxs-lookup"><span data-stu-id="60f29-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="60f29-116">Nesse caso, o driver inicia uma instância do Notepad.exe e Obtém um elemento Automation (ou seja, um objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="60f29-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="60f29-117">Em seguida, o driver cria um objeto de biblioteca de teste de automação da interface do usuário com base na plataforma de interface do usuário que está sendo testada e, em seguida, passa no elemento Automation como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="60f29-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="60f29-118">A biblioteca de testes de automação da interface do usuário determina que o elemento Automation é um tipo de controle de [documento](uiauto-supportdocumentcontroltype.md) e, em seguida, executa os testes de controle de documento, os testes de padrão de controle de [texto](uiauto-implementingtextandtextrange.md) e [rolagem](uiauto-implementingscroll.md) e os testes de elemento de automação genérica.</span><span class="sxs-lookup"><span data-stu-id="60f29-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![Diagrama que mostra o fluxo do driver para o aplicativo para driver a ser UIATestLibrarydo usando setas vermelhas.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="60f29-120">Registro em log com a biblioteca de teste de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="60f29-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="60f29-121">A biblioteca de testes de automação da interface do usuário usa DLLs externas para registrar resultados de execuções de teste.</span><span class="sxs-lookup"><span data-stu-id="60f29-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="60f29-122">Ele dá suporte ao registro em log como XML e registro em log no console.</span><span class="sxs-lookup"><span data-stu-id="60f29-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="60f29-123">Log XML</span><span class="sxs-lookup"><span data-stu-id="60f29-123">XML Logging</span></span>

<span data-ttu-id="60f29-124">Em geral, o log XML é usado pela verificação da automação da interface do usuário visual, mas também pode ser incorporado a um fluxo de trabalho de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="60f29-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="60f29-125">Se o log XML for especificado, o aplicativo de driver deverá serializar a saída criando um objeto **XmlWriter** e passando-o para o método **XmlLog. GetTestRunXml** .</span><span class="sxs-lookup"><span data-stu-id="60f29-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="60f29-126">O driver pode usar o XML serializado internamente ou gravá-lo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="60f29-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="60f29-127">As DLLs a seguir são necessárias para o log XML.</span><span class="sxs-lookup"><span data-stu-id="60f29-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="60f29-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="60f29-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="60f29-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="60f29-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="60f29-130">Log de console</span><span class="sxs-lookup"><span data-stu-id="60f29-130">Console Logging</span></span>

<span data-ttu-id="60f29-131">Por padrão, a biblioteca de testes de automação de interface do usuário usa o log de console, onde toda a saída de log é canalizada como texto sem formatação para a janela do console.</span><span class="sxs-lookup"><span data-stu-id="60f29-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="60f29-132">WUIALogging.dll é necessário para o log do console.</span><span class="sxs-lookup"><span data-stu-id="60f29-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="60f29-133">Requisitos de código para registro em log</span><span class="sxs-lookup"><span data-stu-id="60f29-133">Code Requirements for Logging</span></span>

<span data-ttu-id="60f29-134">Um aplicativo de driver deve incluir os seguintes trechos de código para usar o log de biblioteca de teste de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60f29-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a><span data-ttu-id="60f29-135">Exemplos de log</span><span class="sxs-lookup"><span data-stu-id="60f29-135">Logging Examples</span></span>

<span data-ttu-id="60f29-136">Os exemplos a seguir demonstram a funcionalidade de log básica e mostram como usar a API de biblioteca de teste de automação da interface do usuário em um aplicativo de driver de automação de teste básico.</span><span class="sxs-lookup"><span data-stu-id="60f29-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




