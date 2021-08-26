---
description: Este aplicativo demonstra como você pode criar um aplicativo de reconhecimento de manuscrito. O Windows Vista SDK fornece versões deste exemplo em C \# e Visual Basic .NET também.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Exemplo de reconhecimento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151c92c9f407461c34ecffb015af179e57b5c9ed4735b36f70c9a4d26c78088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935116"
---
# <a name="ink-recognition-sample"></a>Exemplo de reconhecimento de tinta

Este aplicativo demonstra como você pode criar um aplicativo de reconhecimento de manuscrito. O Windows Vista SDK fornece versões deste exemplo em C \# e Visual Basic .NET também. Este tópico refere-se ao exemplo Visual Basic .NET, mas os conceitos são os mesmos entre as versões.

## <a name="access-the-tablet-pc-interfaces"></a>Acessar as interfaces de tablet pc

Primeiro, consulte a API do Tablet PC, que são instaladas com o SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inicializar o InkCollector

O exemplo adiciona código ao manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário que serve para associar [o InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, à janela da caixa de grupo e habilitar o InkCollector.


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>Reconhecer os traços

O [manipulador de](/dotnet/api/system.windows.forms.button?view=netcore-3.1) eventos Click do objeto Button verifica para garantir que o usuário tenha pelo menos um reconhecedor instalado examinando a propriedade [Count](/previous-versions/ms828521(v=msdn.10)) da coleção [Recognizers.](/previous-versions/ms828520(v=msdn.10)) [](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1)

A [propriedade SelectedText](/previous-versions/windows/) da caixa de texto é definida como a melhor combinação para os traços usando o [método ToString](/previous-versions/ms827836(v=msdn.10)) na coleção [Strokes.](/previous-versions/ms552701(v=vs.100)) Depois que os traços foram reconhecidos, eles são excluídos. Por fim, o código força a reintação da área de desenho, limpando-a para uso posterior de tinta.


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
