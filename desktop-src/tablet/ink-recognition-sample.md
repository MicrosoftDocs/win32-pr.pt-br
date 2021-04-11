---
description: Este aplicativo demonstra como você pode criar um aplicativo de reconhecimento de manuscrito. O SDK do Windows Vista fornece versões deste exemplo em C \# e Visual Basic .net também.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Exemplo de reconhecimento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164433"
---
# <a name="ink-recognition-sample"></a>Exemplo de reconhecimento de tinta

Este aplicativo demonstra como você pode criar um aplicativo de reconhecimento de manuscrito. O SDK do Windows Vista fornece versões deste exemplo em C \# e Visual Basic .net também. Este tópico refere-se ao exemplo Visual Basic .NET, mas os conceitos são os mesmos entre as versões.

## <a name="access-the-tablet-pc-interfaces"></a>Acessar as interfaces do Tablet PC

Primeiro, referencie a API do Tablet PC, que é instalada com o SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Inicializar o InkCollector

O exemplo adiciona código ao manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário que serve para associar o [InkCollector](/previous-versions/ms583683(v=vs.100)), myinkcollector, com a janela de caixa de grupo e habilitar o InkCollector.


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

O manipulador de eventos [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) do objeto [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) verifica se o usuário tem pelo menos um reconhecedor instalado examinando a propriedade [Count](/previous-versions/ms828521(v=msdn.10)) da coleção [Recognizers](/previous-versions/ms828520(v=msdn.10)) .

A propriedade [SelectedText](/previous-versions/windows/) da caixa de texto é definida como a melhor correspondência para os traços usando o método [ToString](/previous-versions/ms827836(v=msdn.10)) na coleção [Strokes](/previous-versions/ms552701(v=vs.100)) . Depois que os traços forem reconhecidos, eles serão excluídos. Por fim, o código força a repintura da área de desenho, limpando-a para uso adicional de tinta.


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

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
