---
description: Este tópico apresenta as APIs de Análise de Tinta.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconhecimento básico e análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4bdfa0d93c25e397caf0f116f0f47b303e9571d342825673572011534404de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111297"
---
# <a name="basic-recognition-and-ink-analysis"></a>Reconhecimento básico e análise de tinta

Este tópico apresenta as APIs de Análise de Tinta.

## <a name="simple-recognition"></a>Reconhecimento simples

A funcionalidade básica exposta pela API de análise de tinta é o acesso aos resultados de reconhecimento de uma determinada peça de tinta. Isso é simples e simples de fazer, conforme mostrado no código de exemplo a seguir.


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



Os resultados da operação de reconhecimento são simplesmente um valor de cadeia de caracteres que representa o valor reconhecido da tinta manuscrita. A API de análise de tinta expõe muito mais funcionalidade de reconhecimento do que apenas a cadeia de caracteres reconhecida, mas essa é a operação mais comum.

## <a name="incremental-recognition"></a>Reconhecimento incremental

O processo de reconhecimento leva tempo para ser concluído, bloqueando o acesso ao aplicativo bloqueando o thread de interface do usuário do aplicativo. Portanto, pode ser caro e frustrante para o usuário final aguardar de forma síncrona os resultados. Muitos aplicativos de Tablet PC exigem o reconhecimento de mais de algumas linhas de tinta e uma abordagem incremental para reconhecer traços em um thread em segundo plano é a estratégia ideal. A vantagem de uma abordagem incremental em vez de uma operação em massa é que ela permite que o reconhecimento dos traços ocorra durante um período de tempo, estendendo o trabalho no thread em segundo plano em vez de de forma síncrona no thread de primeiro plano. Para dar suporte à análise incremental, o objeto [**InkAnalyzer**](inkanalyzer.md) tem um método [**BackgroundAnalyze,**](iinkanalyzer-backgroundanalyze.md) que lida com a criação e o gerenciamento de um thread em segundo plano para o aplicativo. O **InkAnalyzer** também cuida automaticamente do gerenciamento do que precisa ser reconhecido e do que já foi reconhecido.

Portanto, há dois mecanismos para obter resultados de reconhecimento:

-   O [**método Analyze**](iinkanalyzer-analyze.md) (análise síncrona), que funciona melhor para:

    -   Pequenas quantidades de tinta.
    -   Quando os resultados são necessários antes de prosseguir para a próxima operação no aplicativo, como ao exibir uma interface do usuário de correção.

-   O [**método BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (análise assíncrona), que funciona melhor para:

    -   Qualquer quantidade de tinta.
    -   Quando utilizado com um temporizador, pulsa aproximadamente a cada 600 milissegundos.

> [!Note]  
> 600 milissegundos é a recomendação atual, mas esse tempo está sujeito a alterações pendentes de testes posteriores.

 

Para usar a operação [**BackgroundAnalyze,**](iinkanalyzer-backgroundanalyze.md) o objeto [**InkCollector**](inkcollector-class.md) (ou objetos ou controles semelhantes, como [**o RTS (RealTimeStylus),**](realtimestylus-class.md) [**InkOverlay**](inkoverlay-class.md)ou [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) no Windows Presentation Foundation) gerencia a coleção e a renderização dos traços de tinta. Se **o InkCollector** estiver emparelhado com as APIs de análise de tinta, os aplicativos poderão manter os resultados de reconhecimento atualizados informando o [**InkAnalyzer**](inkanalyzer.md) sobre cada novo traço adicionado ao aplicativo. Isso permite que o **InkAnalyzer** reconheça os traços incrementalmente e em um thread em segundo plano.

Para realizar a análise incremental em segundo plano, os aplicativos precisam implementar três etapas (mostradas para código gerenciado):

1. Adicione o traço ao [**InkAnalyzer sempre**](inkanalyzer.md) que [](inkoverlay-stroke.md) o evento Stroke do objeto [**InkOverlay**](inkoverlay-class.md) for gerado:


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. Invoque [**as operações BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) em um intervalo definido.


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> Observação Os aplicativos não devem simplesmente invocar a operação de análise em segundo plano após cada novo traço. Isso falhará (retornando um valor de **false**) se uma operação em segundo plano já estiver em execução. O motivo para esse comportamento é limitar o número de threads em segundo plano e as operações de reconciliação necessárias.

 

3. Escutar o evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (código gerenciado) ou o evento [**Results**](-ianalysisevents-results.md) (código C++) para determinar quando o processo em segundo plano foi concluído:


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



Agora que o processamento da tinta está sendo feito em um thread em segundo plano, o aplicativo tem a capacidade de aceitar alterações na tinta enquanto a operação em segundo plano está funcionando. Se usarmos um thread síncrono, isso não será possível. O trabalho é executado no thread da interface do usuário, bloqueando a capacidade de fazer alterações. As alterações incluem adicionar mais tinta ao documento, excluir tinta ou transformar o local ou a aparência da tinta existente. As alterações que ocorrem durante a operação em segundo plano podem, na verdade, invalidar os resultados. Por exemplo, a exclusão de um traço de uma palavra altera o valor de reconhecimento dessa palavra. A API [**inkAnalyzer**](inkanalyzer.md) tem um processo de reconciliação integrado que determina automaticamente quais partes da operação em segundo plano se tornam inválidas como resultado da alteração da tinta durante a análise.

O processo de reconciliação automática é realizado devido a três fatores:

1.  A [**propriedade DirtyRegion.**](iinkanalyzer-getdirtyregion.md)

    -   Sempre que o aplicativo adiciona ([**método AddStrke)**](iinkanalyzer-addstroke.md) ou remove ([**método RemoveStrke)**](iinkanalyzer-removestroke.md) um traço para ou do [**InkAnalyzer**](inkanalyzer.md), o local físico do traço é capturado e, na próxima vez que uma operação de análise é invocada, o **InkAnalyzer** garante que o traço ou a área ocupada por esse traço seja analisada.
    -   Sempre que o aplicativo modifica a tinta existente, altera o local ou altera outros atributos de desenho da tinta, o local da alteração (os limites da tinta) pode ser adicionado à propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) do [**InkAnalyzer.**](inkanalyzer.md) Isso garante que, na próxima vez que o aplicativo iniciar a operação de análise, essas áreas serão verificadas quanto aos resultados corretos.
    -   Portanto, a propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) controla, entre as executações de análise, quais áreas do documento e quais traços precisam ser verificados quanto aos resultados corretos de reconhecimento e análise de tinta.

2.  Análise limitada.

    -   Sempre que o aplicativo invoca a operação de análise, a propriedade [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica quais traços precisam ser analisados. Isso permite que a operação de análise limite a operação somente às regiões sujas e ignore todas as outras regiões, otimizando a quantidade de tempo gasto revisando tinta.
    -   O [**InkAnalyzer**](inkanalyzer.md) não ignora completamente todas as outras regiões na página, mas, em vez disso, pode examinar áreas vizinhos para determinar se as alterações feitas na região suja afetam essas regiões vizinhos. Por exemplo, o analisador classifica "Is", no exemplo de tinta a seguir, como um único tipo **InkWord** da [**classe ContextNode:**](icontextnode.md)

![manuscrito "is"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

Excluir os "s" resulta em uma região suja (marcada com uma caixa vermelha).

![manuscrito "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Após a análise, o analisador altera a classificação do "I" para um tipo **InkDrawing,** mesmo que ele seja fora da região suja, porque sem o traço "s" de suporte, o analisador de tinta tem uma chance de 50/50 de a tinta ser classificada como um desenho ou uma palavra.

-   Estado armazenado em cache internamente.

    -   Quando um aplicativo invoca uma operação de análise em segundo plano, [**o InkAnalyzer**](inkanalyzer.md) armazena em cache um instantâneo dos dados remoção. Ao tirar um instantâneo, o **InkAnalyzer** pode trabalhar na análise dos dados independentemente dos dados que estão sendo usados pelo aplicativo ou usar o instantâneo como ponto de comparação para determinar quais alterações foram feitas pelo aplicativo durante a análise em segundo plano.
    -   Caching o estado e comparar alterações é melhor do que manter uma lista de todas as alterações ocorridas por um motivo principal: proxy de dados. Este é um cenário avançado descrito posteriormente neste documento, mas envolve o aplicativo atualizando o [**InkAnalyzer**](inkanalyzer.md) apenas com os dados atuais de tinta e não tinta antes da operação de análise invocada e antes de processar os resultados de uma operação de análise.

## <a name="simple-ink-analysis"></a>Análise de tinta simples

Os dois cenários anteriores (reconhecimento simples e reconhecimento incremental) descrevem como acessar valores de reconhecimento, mas não mencionam como acessar a análise de tinta ou os resultados da classificação. A configuração padrão do [**InkAnalyzer**](inkanalyzer.md)executa algoritmos de análise de tinta e algoritmos de reconhecimento. Essa configuração gera os resultados mais precisos, pois as duas tecnologias trabalham juntas para aumentar a precisão. Ou seja, os mecanismos de análise de tinta ajudam a separar o desenho da escrita e normalizar a escrita emaranhada em um plano horizontal, que é o plano de entrada ideal para os mecanismos de reconhecimento.

Para acessar os resultados da análise de tinta, seu aplicativo usa os métodos [**Analyze**](iinkanalyzer-analyze.md) ou [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exatamente como descrito nos dois cenários de reconhecimento anteriores. Nada muda porque os algoritmos de reconhecimento e análise de tinta já estão sendo executados quando esses métodos são chamados. No entanto, acessar os resultados é mais complicado do que ler o valor de uma cadeia de caracteres. Por exemplo, o exemplo de código a seguir mostra o grupo e os locais de todos os segmentos **InkWord** e **InkDrawing** renderização de um retângulo em torno do grupo de traços que composição da classificação.

Este exemplo simplesmente usa o evento Paint **formulário** para renderizar retângulos coloridos em torno das palavras ou desenhos. O [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) retornará uma coleção de objetos que existe somente se a operação de análise tiver sido executada e os resultados contêm classificações com o tipo [**ContextNode**](icontextnode.md) especificado. Se nenhum **ContextNode** do tipo desejado existir no documento, as etapas para desenhar os retângulos serão ignoradas.

Cada objeto retornado do [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) terá propriedades relacionadas a esse tipo de classificação. Por exemplo, **InkWordNode** faz referência a todos os traços que comem uma única palavra no documento e faz referência à cadeia de caracteres reconhecida para essa palavra. O **InkDrawingNode** faz referência a todos os traços que comem o único desenho no documento e faz referência ao nome da forma para esse desenho.

O [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) é muito semelhante ao [**método DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) que retornou coleções de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de tipos de escrita ou desenho.


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



Para colocar o exemplo de código anterior em perspectiva, considere o seguinte exemplo de tinta:

![amostra de tinta "este é um pouco de tinta". com um círculo abaixo dele](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Se você chamar [**o método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e passar o campo estático para **InkWord,** o analisador retornará uma coleção de quatro **objetos InkWordNode:**

![saída do analisador, "este é um pouco de tinta"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Se você chamar [**o método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) e passar o campo estático **para InkDrawing,** o analisador retornará uma coleção de um **objeto InkDrawingNode:**

![imagem mostrando "oval", o resultado do analisador inkdrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Depois que **Paint** evento tiver sido acionado, o código de exemplo renderizará retângulos em torno de cada um dos objetos:

![desenho original com retângulos renderizados em torno do objeto e palavras](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Este exemplo toca apenas no método [**FindNodesOfType,**](iinkanalyzer-findnodesoftype.md) mas como os mecanismos de análise de tinta podem detectar um conjunto mais rico de tipos de tinta, o método também corresponde a todos os tipos de nós detectáveis pelos mecanismos de análise de tinta (como linhas, parágrafos e outras estruturas).

## <a name="using-ink-analysis-with-point-erase"></a>Usando a análise de tinta com a apagação de ponto

Seu aplicativo precisa fazer ajustes na maneira como ele atualiza os traços ao executar apagamento de ponto para garantir um bom desempenho. Em primeiro lugar, na camada de aplicativo, substitua o ponto de caneta do Traço existente pelo ponto de caneta do novo traço e, em seguida, chame [**ClearStrkeData**](iinkanalyzer-clearstrokedata.md) nesse traço e atualize a região suja com os limites do traço. Isso fará com que [**o InkAnalyzer**](inkanalyzer.md) busque os dados de traço atualizados quando a próxima rodada de análise em segundo plano for iniciada. Essa técnica é demonstrada no exemplo a seguir.


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da análise de tinta](ink-analysis-overview.md)
</dt> <dt>

[Uso da API de Análise de Tinta](ink-analysis-api-usage.md)
</dt> </dl>

 

 
