---
description: Este exemplo mostra como usar a análise de tinta para criar um aplicativo de preenchimento de formulário, onde o formulário é baseado em um formulário de papel digitalizado.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulário de papel examinado da análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718642"
---
# <a name="ink-analysis-scanned-paper-form"></a>Formulário de papel examinado da análise de tinta

Este exemplo mostra como usar a análise de tinta para criar um aplicativo de preenchimento de formulário, onde o formulário é baseado em um formulário de papel digitalizado.

## <a name="features-demonstrated"></a>Recursos demonstrados

este aplicativo de exemplo demonstra os seguintes recursos da API de análise de tinta e os controles de tinta de Windows Forms:

-   Carregando um formulário de papel digitalizado. O exemplo importa o formulário de uma imagem no formato .png.
-   Coleta e renderização de tinta sobre o formulário digitalizado.
-   Usando um objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analisar manuscrito.
-   Gerando objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) para melhorar os resultados de manuscrito.
-   Populando caixas de texto de dicas de análise.
-   Criação de uma experiência básica de correção de texto.

## <a name="project-references"></a>Referências de Projeto

o exemplo está disponível como um aplicativo Windows Forms ou Windows Presentation Foundation. a versão Windows Forms faz referência a:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

a versão Windows Presentation Foundation faz referência a IAWinFX.dll além das dlls principais do Windows Presentation Foundation.

> [!Note]  
> a versão Windows Presentation Foundation deste exemplo (encontrada no diretório XAML) requer que as extensões de Windows Presentation Foundation para Microsoft Visual Studio 2005 estejam instaladas no sistema.

 

## <a name="user-interface"></a>Interface do Usuário

A interface do usuário para esse aplicativo consiste em um [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) com dois objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associados a ele: formulário de tinta e formulário de texto convertido. A guia formulário de tinta contém

-   Um painel que contém uma imagem de um formulário de papel digitalizado usado para fazer mensagens telefônicas.
-   Uma caixa de seleção que tem o aplicativo mostrará os limites da dica de análise quando selecionado.
-   Um par de botões, limpar e analisar, que limpam a tinta do formulário e inicializam a análise de tinta.

O formulário de texto convertido contém a mesma imagem e é a página na qual o aplicativo exibe o texto reconhecido. Quando você clica em analisar, o aplicativo executa a análise de tinta de forma síncrona e os resultados de reconhecimento aparecem na guia formulário de texto convertido.

## <a name="functionality"></a>Funcionalidade

Esse aplicativo usa um [InkOverlay](/previous-versions/ms552322(v=vs.100)) para habilitar a gravação. O objeto InkOverlay é adequado para observações e scribbling básicas. O uso pretendido principal deste objeto é exibir a tinta como tinta. A classe principal para análise de tinta é a classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) . Quando você chama o método [Analyze](/previous-versions/ms568971(v=vs.100)) do objeto InkAnalyzer, a análise de tinta ocorre de forma síncrona.

O aplicativo Inicializa duas matrizes, uma das cadeias de caracteres e um dos retângulos. A matriz de cadeia `factoidStrings` de caracteres,, é feita de objetos [facto](/previous-versions/ms583657(v=vs.100)) que são passados para o [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) . Os objetos AnalysisHintNode ajustam a InkAnalyzer em direção à entrada específica. Este exemplo usa as dicas de data, hora e telefone, bem como outras.

Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) é associado a uma área específica do formulário. As áreas são representadas pela matriz de retângulos, `rects` . Ao criar uma [caixa de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) para cada retângulo, o exemplo gera o texto reconhecido no local correto.


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



Depois disso, é meramente uma questão de criar um manipulador de eventos que dispara a análise de tinta quando o usuário clica em analisar.


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
