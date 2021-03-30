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
# <a name="custom-verification-routines"></a>Rotinas de verificação personalizadas

Esta seção descreve como criar uma rotina de verificação personalizada para a ferramenta AccChecker (verificador de acessibilidade da interface do usuário).

-   [Criando uma verificação personalizada](#creating-a-custom-verification)
    -   [Exemplo de verificação personalizada](#sample-custom-verification)
-   [Usando uma verificação personalizada](#using-a-custom-verification)
    -   [A GUI (interface gráfica do usuário) do AccChecker](#the-accchecker-graphical-user-interface-gui)
    -   [Automação do AccChecker](#accchecker-automation)
-   [Tópicos relacionados](#related-topics)

O AccChecker (verificador de acessibilidade da interface do usuário) é uma ferramenta de teste de acessibilidade projetada para verificar a implementação do Microsoft Acessibilidade Ativa (MSAA) em uma interface do usuário do aplicativo ou controle. Problemas de acessibilidade de alto impacto que podem ser expostos pela implementação de MSAA são testados com um conjunto de rotinas de verificação automatizadas internas. Essas rotinas de verificação nativa podem ser aumentadas com rotinas personalizadas usando a plataforma AccChecker extensível.

## <a name="creating-a-custom-verification"></a>Criando uma verificação personalizada

Uma verificação personalizada é criada como uma biblioteca de classes (DLL) que implementa uma única interface ( `IVerificationRoutine` ) que contém um membro ( `Execute` ):


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parâmetros**

*HWND*

Tipo: **System. IntPtr**

O HWND do elemento que está sendo verificado.

*digita*

Tipo: **AccCheck. Logging. ILogger**

O método de log selecionado. Os tipos possíveis incluem **AccumulatingLogger** (usado pelo AccChecker para armazenar em cache todas as entradas de log até que as verificações sejam concluídas), **ConsoleLogger**, **TextFileLogger** e **XMLSerializingLogger**.

*AllowUI*

Tipo: **bool**

Indica se a rotina de verificação exibe a interface do usuário que está testando. Geralmente definido como falso em cenários de teste automatizado.

*gráficos*

Tipo: **AccCheck. GraphicsHelper**

Usado para capturas de tela e outras visualizações no AccChecker.

### <a name="sample-custom-verification"></a>Exemplo de verificação personalizada

O exemplo a seguir é uma verificação personalizada em C# que executa uma verificação de profundidade de árvore de elementos simples. Um erro será registrado se a árvore de elementos for maior que 50 níveis de profundidade, um aviso será registrado se a árvore de elementos for de 20 a 50 níveis de profundidade e uma mensagem informativa será registrada de outra forma.


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
> Uma solução Microsoft Visual Studio que contém o código de exemplo de verificação está incluída na documentação da ajuda. Os arquivos estão localizados no caminho de instalação do AccChecker.

 

## <a name="using-a-custom-verification"></a>Usando uma verificação personalizada

Esta seção descreve como incorporar uma verificação personalizada em cenários de teste do AccChecker.

### <a name="the-accchecker-graphical-user-interface-gui"></a>A GUI (interface gráfica do usuário) do AccChecker

Para incluir uma rotina de verificação personalizada no aplicativo AccChecker, basta clicar em abrir DLL no menu arquivo e localizar a DLL para a rotina. A rotina personalizada será adicionada à parte inferior da lista de verificações no painel Selecionar rotinas de verificação.

A captura de tela a seguir mostra a verificação personalizada de profundidade da árvore de verificação de exemplo adicionada a AccChecker.

![exemplo de rotina de verificação personalizada de profundidade da árvore de verificação adicionada à interface do usuário do amaccchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Se os valores de atributo de verificação não forem especificados na rotina de verificação personalizada, a verificação ainda será carregada em AccChecker, mesmo que não apareça na interface do usuário. Como não é exibido na interface do usuário, ele não pode ser desmarcado e excluído das execuções de verificação subsequentes.

 

### <a name="accchecker-automation"></a>Automação do AccChecker

Incorporar uma rotina de verificação personalizada em uma estrutura AccChecker automatizada é tão simples quanto adicionar a DLL de verificação e habilitar as rotinas de verificação desejadas.

O trecho de código a seguir demonstra como usar a API AccChecker para testar a funcionalidade de tabulação no aplicativo do painel de controle do firewall do Windows.


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
> Uma solução Microsoft Visual Studio 2008 que contém o código de exemplo de verificação está incluída na documentação da ajuda. Os arquivos estão localizados no caminho de instalação do AccChecker.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




