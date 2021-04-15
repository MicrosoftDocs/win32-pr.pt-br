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
# <a name="ui-automation-test-library"></a>Biblioteca de teste de automação da interface do usuário

A biblioteca de testes de automação da interface do usuário (biblioteca de teste UIA) é uma API que é chamada pelo aplicativo de *Driver* em um cenário de teste automatizado. O driver é o aplicativo que obtém um elemento Automation (objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) de um controle que requer verificação e o fornece à biblioteca de teste de automação da interface do usuário. Em seguida, a biblioteca de testes verifica e valida a implementação da automação da interface do usuário. Para saber mais sobre automação da interface do usuário e elementos de automação, confira [conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md).

-   [Fluxo de trabalho da biblioteca de teste de automação da IU](#ui-automation-test-library-workflow)
-   [Registro em log com a biblioteca de teste de automação da interface do usuário](#logging-with-the-ui-automation-test-library)
    -   [Log XML](#xml-logging)
    -   [Log de console](#console-logging)
    -   [Requisitos de código para registro em log](#code-requirements-for-logging)
    -   [Exemplos de log](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Fluxo de trabalho da biblioteca de teste de automação da IU

O diagrama a seguir mostra um fluxo de trabalho de teste que incorpora a biblioteca de teste de automação da interface do usuário usando um aplicativo de console como o driver. Nesse caso, o driver inicia uma instância do Notepad.exe e Obtém um elemento Automation (ou seja, um objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) do controle de edição. Em seguida, o driver cria um objeto de biblioteca de teste de automação da interface do usuário com base na plataforma de interface do usuário que está sendo testada e, em seguida, passa no elemento Automation como um parâmetro. A biblioteca de testes de automação da interface do usuário determina que o elemento Automation é um tipo de controle de [documento](uiauto-supportdocumentcontroltype.md) e, em seguida, executa os testes de controle de documento, os testes de padrão de controle de [texto](uiauto-implementingtextandtextrange.md) e [rolagem](uiauto-implementingscroll.md) e os testes de elemento de automação genérica.

![Diagrama que mostra o fluxo do driver para o aplicativo para driver a ser UIATestLibrarydo usando setas vermelhas.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Registro em log com a biblioteca de teste de automação da interface do usuário

A biblioteca de testes de automação da interface do usuário usa DLLs externas para registrar resultados de execuções de teste. Ele dá suporte ao registro em log como XML e registro em log no console.

### <a name="xml-logging"></a>Log XML

Em geral, o log XML é usado pela verificação da automação da interface do usuário visual, mas também pode ser incorporado a um fluxo de trabalho de linha de comando.

Se o log XML for especificado, o aplicativo de driver deverá serializar a saída criando um objeto **XmlWriter** e passando-o para o método **XmlLog. GetTestRunXml** . O driver pode usar o XML serializado internamente ou gravá-lo em um arquivo.

As DLLs a seguir são necessárias para o log XML.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Log de console

Por padrão, a biblioteca de testes de automação de interface do usuário usa o log de console, onde toda a saída de log é canalizada como texto sem formatação para a janela do console. WUIALogging.dll é necessário para o log do console.

### <a name="code-requirements-for-logging"></a>Requisitos de código para registro em log

Um aplicativo de driver deve incluir os seguintes trechos de código para usar o log de biblioteca de teste de automação da interface do usuário.


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



### <a name="logging-examples"></a>Exemplos de log

Os exemplos a seguir demonstram a funcionalidade de log básica e mostram como usar a API de biblioteca de teste de automação da interface do usuário em um aplicativo de driver de automação de teste básico.


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



 

 




