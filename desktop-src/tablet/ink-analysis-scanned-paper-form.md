---
description: Este exemplo mostra como usar a análise de tinta para criar um aplicativo de preenchimento de formulário, onde o formulário é baseado em um formulário de papel digitalizado.
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: Formulário de papel examinado da análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164300"
---
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="5151f-103">Formulário de papel examinado da análise de tinta</span><span class="sxs-lookup"><span data-stu-id="5151f-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="5151f-104">Este exemplo mostra como usar a análise de tinta para criar um aplicativo de preenchimento de formulário, onde o formulário é baseado em um formulário de papel digitalizado.</span><span class="sxs-lookup"><span data-stu-id="5151f-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="5151f-105">Recursos demonstrados</span><span class="sxs-lookup"><span data-stu-id="5151f-105">Features Demonstrated</span></span>

<span data-ttu-id="5151f-106">Este aplicativo de exemplo demonstra os seguintes recursos da API de análise de tinta e os controles de tinta de Windows Forms:</span><span class="sxs-lookup"><span data-stu-id="5151f-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="5151f-107">Carregando um formulário de papel digitalizado.</span><span class="sxs-lookup"><span data-stu-id="5151f-107">Loading a scanned paper form.</span></span> <span data-ttu-id="5151f-108">O exemplo importa o formulário de uma imagem no formato. png.</span><span class="sxs-lookup"><span data-stu-id="5151f-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="5151f-109">Coleta e renderização de tinta sobre o formulário digitalizado.</span><span class="sxs-lookup"><span data-stu-id="5151f-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="5151f-110">Usando um objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) para analisar manuscrito.</span><span class="sxs-lookup"><span data-stu-id="5151f-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="5151f-111">Gerando objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) para melhorar os resultados de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="5151f-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="5151f-112">Populando caixas de texto de dicas de análise.</span><span class="sxs-lookup"><span data-stu-id="5151f-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="5151f-113">Criação de uma experiência básica de correção de texto.</span><span class="sxs-lookup"><span data-stu-id="5151f-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="5151f-114">Referências de Projeto</span><span class="sxs-lookup"><span data-stu-id="5151f-114">Project References</span></span>

<span data-ttu-id="5151f-115">O exemplo está disponível como um aplicativo Windows Forms ou Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="5151f-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="5151f-116">A versão Windows Forms faz referência a:</span><span class="sxs-lookup"><span data-stu-id="5151f-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="5151f-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="5151f-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="5151f-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="5151f-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="5151f-119">A versão Windows Presentation Foundation faz referência a IAWinFX.dll além das DLLs principais do Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="5151f-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="5151f-120">A versão Windows Presentation Foundation deste exemplo (encontrada no diretório XAML) requer que as extensões de Windows Presentation Foundation para Microsoft Visual Studio 2005 estejam instaladas no sistema.</span><span class="sxs-lookup"><span data-stu-id="5151f-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="5151f-121">Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="5151f-121">User Interface</span></span>

<span data-ttu-id="5151f-122">A interface do usuário para esse aplicativo consiste em um [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) com dois objetos [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) associados a ele: formulário de tinta e formulário de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="5151f-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="5151f-123">A guia formulário de tinta contém</span><span class="sxs-lookup"><span data-stu-id="5151f-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="5151f-124">Um painel que contém uma imagem de um formulário de papel digitalizado usado para fazer mensagens telefônicas.</span><span class="sxs-lookup"><span data-stu-id="5151f-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="5151f-125">Uma caixa de seleção que tem o aplicativo mostrará os limites da dica de análise quando selecionado.</span><span class="sxs-lookup"><span data-stu-id="5151f-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="5151f-126">Um par de botões, limpar e analisar, que limpam a tinta do formulário e inicializam a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="5151f-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="5151f-127">O formulário de texto convertido contém a mesma imagem e é a página na qual o aplicativo exibe o texto reconhecido.</span><span class="sxs-lookup"><span data-stu-id="5151f-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="5151f-128">Quando você clica em analisar, o aplicativo executa a análise de tinta de forma síncrona e os resultados de reconhecimento aparecem na guia formulário de texto convertido.</span><span class="sxs-lookup"><span data-stu-id="5151f-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="5151f-129">Funcionalidade</span><span class="sxs-lookup"><span data-stu-id="5151f-129">Functionality</span></span>

<span data-ttu-id="5151f-130">Esse aplicativo usa um [InkOverlay](/previous-versions/ms552322(v=vs.100)) para habilitar a gravação.</span><span class="sxs-lookup"><span data-stu-id="5151f-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="5151f-131">O objeto InkOverlay é adequado para observações e scribbling básicas.</span><span class="sxs-lookup"><span data-stu-id="5151f-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="5151f-132">O uso pretendido principal deste objeto é exibir a tinta como tinta.</span><span class="sxs-lookup"><span data-stu-id="5151f-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="5151f-133">A classe principal para análise de tinta é a classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="5151f-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="5151f-134">Quando você chama o método [Analyze](/previous-versions/ms568971(v=vs.100)) do objeto InkAnalyzer, a análise de tinta ocorre de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="5151f-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="5151f-135">O aplicativo Inicializa duas matrizes, uma das cadeias de caracteres e um dos retângulos.</span><span class="sxs-lookup"><span data-stu-id="5151f-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="5151f-136">A matriz de cadeia `factoidStrings` de caracteres,, é feita de objetos [facto](/previous-versions/ms583657(v=vs.100)) que são passados para o [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) como objetos [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="5151f-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="5151f-137">Os objetos AnalysisHintNode ajustam a InkAnalyzer em direção à entrada específica.</span><span class="sxs-lookup"><span data-stu-id="5151f-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="5151f-138">Este exemplo usa as dicas de data, hora e telefone, bem como outras.</span><span class="sxs-lookup"><span data-stu-id="5151f-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="5151f-139">Cada [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) é associado a uma área específica do formulário.</span><span class="sxs-lookup"><span data-stu-id="5151f-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="5151f-140">As áreas são representadas pela matriz de retângulos, `rects` .</span><span class="sxs-lookup"><span data-stu-id="5151f-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="5151f-141">Ao criar uma [caixa de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) para cada retângulo, o exemplo gera o texto reconhecido no local correto.</span><span class="sxs-lookup"><span data-stu-id="5151f-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


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



<span data-ttu-id="5151f-142">Depois disso, é meramente uma questão de criar um manipulador de eventos que dispara a análise de tinta quando o usuário clica em analisar.</span><span class="sxs-lookup"><span data-stu-id="5151f-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


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



 

 
