---
description: Este exemplo mostra como usar a Análise de Tinta Digital para criar um aplicativo de preenchimento de formulário, em que o formulário é baseado em um formulário de papel digitalizado.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulário de papel digitalizado de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4069efd5ba8763e00e9b3170ffb0a39a4a70c4d66d07d3c8bf08bc3688f57ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718642"
---
# <a name="ink-analysis-scanned-paper-form"></a>Formulário de papel digitalizado de análise de tinta

Este exemplo mostra como usar a Análise de Tinta Digital para criar um aplicativo de preenchimento de formulário, em que o formulário é baseado em um formulário de papel digitalizado.

## <a name="features-demonstrated"></a>Recursos demonstrados

Este aplicativo de exemplo demonstra os seguintes recursos da API de Análise de Tinta e os controles de tinta Windows Forms:

-   Carregando um formulário de papel digitalizado. O exemplo importa o formulário de uma imagem em .png formato.
-   Coletando e renderizando tinta sobre o formulário digitalizado.
-   Usando um [objeto InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analisar o manuscrito.
-   Gerando [objetos AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) para melhorar os resultados de manuscrito.
-   Preenchendo caixas de texto de dicas de análise.
-   Criando uma experiência básica de correção de texto.

## <a name="project-references"></a>Referências de Projeto

O exemplo está disponível como um aplicativo Windows Forms ou Windows Presentation Foundation aplicativo. As referências Windows versão do Windows Forms:

-   Microsoft.Ink.dll
-   Microsoft.Ink.Analysis.dll

A Windows Presentation Foundation de versão IAWinFX.dll além das dlls Windows Presentation Foundation núcleo.

> [!Note]  
> A Windows Presentation Foundation deste exemplo (encontrada no diretório XAML) requer que as extensões Windows Presentation Foundation do Microsoft Visual Studio 2005 estão instaladas no sistema.

 

## <a name="user-interface"></a>Interface do Usuário

A interface do usuário desse aplicativo consiste em [um TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) com dois objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associados a ele: Formulário de Tinta e Formulário de Texto Convertido. A guia Formulário de Tinta Contém

-   Um painel que contém uma imagem de um formulário de papel digitalizado usado para receber mensagens telefônicas.
-   Uma caixa de seleção que tem o aplicativo mostra os limites da dica de análise quando selecionado.
-   Um par de botões, Limpar e Analisar, que limpam a tinta do formulário e inicializam a análise de tinta.

O Formulário de Texto Convertido contém a mesma imagem e é a página na qual o aplicativo exibe o texto reconhecido. Quando você clica em Analisar, o aplicativo executa a análise de tinta de forma síncrona e os resultados de reconhecimento aparecem na guia Formulário de Texto Convertido.

## <a name="functionality"></a>Funcionalidade

Esse aplicativo usa um [InkOverlay para](/previous-versions/ms552322(v=vs.100)) habilitar a escrita. O objeto InkOverlay é adequado para anotações e rabiscos básicos. O principal uso pretendido desse objeto é exibir tinta como tinta. A classe principal para análise de tinta é a [classe InkAnalyzer.](/previous-versions/ms583671(v=vs.100)) Quando você chama o método [Analyze](/previous-versions/ms568971(v=vs.100)) do objeto InkAnalyzer, a análise de tinta ocorre de forma síncrona.

O aplicativo inicializa duas matrizes, uma de cadeias de caracteres e uma de retângulos. A matriz de cadeia de caracteres, , é feita de objetos Factoid que são passados para `factoidStrings` [o InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como [objetos AnalysisHintNode.](/previous-versions/ms573018(v=vs.100)) [](/previous-versions/ms583657(v=vs.100)) Os objetos AnalysisHintNode são desvios do InkAnalyzer para uma entrada específica. Este exemplo usa as dicas de data, hora e telefone, bem como algumas outras.

Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) está associado a uma área específica do formulário. As áreas são representadas pela matriz de retângulos, `rects` . Ao criar uma [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) para cada retângulo, o exemplo gera o texto reconhecido no local correto.


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



Depois disso, é simplesmente uma questão de criar um manipulador de eventos que dispara a análise de tinta quando o usuário clica em Analisar.


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



 

 
