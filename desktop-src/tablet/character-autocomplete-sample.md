---
description: O exemplo de preenchimento automático demonstra como implementar o preenchimento automático de caracteres em Japonês usando as APIs (interfaces de programação de aplicativo) de reconhecimento.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Exemplo de preenchimento automático de caractere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501137"
---
# <a name="character-autocomplete-sample"></a>Exemplo de preenchimento automático de caractere

O exemplo de preenchimento automático demonstra como implementar o preenchimento automático de caracteres em Japonês usando as APIs (interfaces de programação de aplicativo) de reconhecimento.

Os recursos a seguir são usados neste exemplo:

-   Usando um *coletor de tinta*
-   Usando um *contexto de reconhecedor*

## <a name="initializing-the-ink-collector-and-recognizer-context"></a>Inicializando o coletor de tinta e o contexto do reconhecedor

Os objetos [**InkCollector**](inkcollector-class.md) e [**InkRecognizerContext**](inkrecognizercontext-class.md) são declarados como classes que podem gerar eventos.


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



O manipulador de eventos Load do formulário cria um coletor de tinta, associa o coletor de tinta à caixa de imagem e habilita a coleta de tinta. Em seguida, o manipulador de eventos carrega o reconhecedor japonês padrão e inicializa o guia do contexto do reconhecedor e as propriedades de traços.


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a>Carregando o reconhecedor japonês padrão

O método [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) é chamado para recuperar o reconhecedor padrão para o idioma japonês. Em seguida, a propriedade [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) do objeto IInkRecognizer é verificada para determinar se o reconhecedor oferece suporte ao idioma japonês. Se tiver, o método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) do Recognizer será usado para gerar um contexto de reconhecedor para o formulário.


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a>Manipulando o evento de traço

O manipulador de eventos [**Stroke**](inkcollector-stroke.md) primeiro interrompe o reconhecimento em segundo plano no contexto do reconhecedor. Em seguida, ele adiciona o novo traço à propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do contexto do reconhecedor. Por fim, ele define a propriedade [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) do contexto do Recognizer e chama o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) do contexto de reconhecedor para cada um dos três modos de preenchimento automático de um caractere. O parâmetro *CustomData* da chamada do método **BackgroundRecognizeWithAlternates** é usado para identificar quais resultados de reconhecimento são retornados no evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) .


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a>Manipulando o evento de reconhecimento com alternativas

O manipulador para o evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) verifica primeiro o parâmetro *RecognitionStatus* . Se houver um erro no reconhecimento, o manipulador de eventos ignorará os resultados de reconhecimento. Caso contrário, o manipulador de eventos adiciona o parâmetro *RecognitionResult* à caixa de imagem apropriada e salva a cadeia de caracteres de resultado. O parâmetro *CustomData* é definido na chamada ao método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) e identifica qual modo de preenchimento automático de caractere foi usado pelo contexto do reconhecedor.


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a>Pintando o formulário

O manipulador de eventos de pintura limpa as caixas de imagem de resultados e adiciona os resultados de reconhecimento salvos a elas.

## <a name="deleting-the-strokes"></a>Excluindo os traços

O método do formulário `CmdClear_Click` manipula o comando de limpeza. Se o [**InkCollector**](inkcollector-class.md) estiver coletando tinta no momento, uma caixa de mensagem será exibida e o comando será ignorado. Caso contrário, o manipulador de eventos interrompe o reconhecimento em segundo plano, limpa a propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) do contexto do reconhecedor e exclui os traços do objeto [**InkDisp**](inkdisp-class.md) do formulário. Em seguida, o manipulador de eventos redesenha a caixa de imagem à qual o coletor de tinta está associado e limpa as cadeias de caracteres e as caixas de imagens de reconhecimento.


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
