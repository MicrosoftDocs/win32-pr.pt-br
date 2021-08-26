---
title: Rotinas de verificação personalizadas
description: Esta seção descreve como criar uma rotina de verificação personalizada para a ferramenta AccChecker (Verificador de Acessibilidade da Interface do Usuário).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245865a0ab4aa6848d4a4361a30febbb341742208586ebf4ec5b35c34fa30534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030876"
---
# <a name="custom-verification-routines"></a>Rotinas de verificação personalizadas

Esta seção descreve como criar uma rotina de verificação personalizada para a ferramenta AccChecker (Verificador de Acessibilidade da Interface do Usuário).

-   [Criando uma verificação personalizada](#creating-a-custom-verification)
    -   [Verificação personalizada de exemplo](#sample-custom-verification)
-   [Usando uma verificação personalizada](#using-a-custom-verification)
    -   [A GUI (guia Interface do Usuário gráfica) do AccChecker](#the-accchecker-graphical-user-interface-gui)
    -   [Automação do AccChecker](#accchecker-automation)
-   [Tópicos relacionados](#related-topics)

O AccChecker (Verificador de Acessibilidade da Interface do Usuário) é uma ferramenta de teste de acessibilidade projetada para verificar a implementação de Microsoft Active Accessibility (MSAA) em um controle ou interface do usuário do aplicativo. Problemas de acessibilidade de alto impacto que podem ser expostos pela implementação da MSAA são testados com um conjunto de rotinas de verificação automatizadas. Essas rotinas de verificação nativas podem ser aumentadas com rotinas personalizadas usando a plataforma extensível AccChecker.

## <a name="creating-a-custom-verification"></a>Criando uma verificação personalizada

Uma verificação personalizada é criada como uma DLL (biblioteca de classes) que implementa uma única interface ( `IVerificationRoutine` ) que contém um membro ( `Execute` ):


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parâmetros**

*Hwnd*

Tipo: **System.IntPtr**

O HWND do elemento que está sendo verificado.

*Logger*

Tipo: **AccCheck.Logging.ILogger**

O método de registro em log selecionado. Os tipos possíveis incluem **AccumulatingLogger** (usado pelo AccChecker para armazenar em cache todas as entradas de log até que as verificações sejam concluídas), **ConsoleLogger,** **TextFileLogger** e **XMLSerializingLogger.**

*AllowUI*

Tipo: **bool**

Indica se a rotina de verificação exibe a interface do usuário que está testando. Geralmente definido como false em cenários de teste automatizados.

*elemento gráfico*

Tipo: **AccCheck.GraphicsHelper**

Usado para capturas de tela e outras visualizações no AccChecker.

### <a name="sample-custom-verification"></a>Verificação personalizada de exemplo

O exemplo a seguir é uma verificação personalizada em C# que executa uma verificação de profundidade de árvore de elemento simples. Um erro será registrado se a árvore de elementos for maior que 50 níveis de profundidade, um aviso será registrado se a árvore de elementos tiver de 20 a 50 níveis de profundidade e uma mensagem informacional for registrada em seu caso.


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
> Uma Microsoft Visual Studio que contém o código de exemplo de verificação está incluída na documentação da ajuda. Os arquivos estão localizados no caminho de instalação do AccChecker.

 

## <a name="using-a-custom-verification"></a>Usando uma verificação personalizada

Esta seção descreve como incorporar uma verificação personalizada em cenários de teste do AccChecker.

### <a name="the-accchecker-graphical-user-interface-gui"></a>A GUI (guia Interface do Usuário gráfica) do AccChecker

Para incluir uma rotina de verificação personalizada no aplicativo AccChecker, basta clicar em Abrir DLL no menu Arquivo e localizar a DLL para a rotina. A rotina personalizada será adicionada à parte inferior da lista de verificações no painel Selecionar rotinas de verificação.

A captura de tela a seguir mostra a verificação personalizada profundidade da árvore de verificação de exemplo adicionada ao AccChecker.

![exemplo de rotina de verificação personalizada da profundidade da árvore adicionada à interface do usuário do accchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Se os valores de atributo de verificação não são especificados na rotina de verificação personalizada, a verificação ainda é carregada no AccChecker, embora não apareça na interface do usuário. Como ele não é exibido na interface do usuário, ele não pode ser desmarcado e excluído das próximas verificações.

 

### <a name="accchecker-automation"></a>Automação do AccChecker

Incorporar uma rotina de verificação personalizada em uma estrutura automatizada do AccChecker é tão simples quanto adicionar a DLL de verificação e habilenciar as rotinas de verificação desejadas.

O snippet de código a seguir demonstra como usar a API do AccChecker para testar a funcionalidade de tabulação no aplicativo Windows painel de controle firewall.


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
> Uma Microsoft Visual Studio 2008 que contém o código de exemplo de verificação está incluída na documentação da ajuda. Os arquivos estão localizados no caminho de instalação do AccChecker.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




