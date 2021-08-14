---
description: Esse aplicativo é baseado no objeto InkCollector e demonstra a coleta de tinta.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Exemplo de coleção de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718255"
---
# <a name="ink-collection-sample"></a>Exemplo de coleção de tinta

Esse aplicativo é baseado no objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) e demonstra a coleta de tinta. O aplicativo cria uma janela, anexa um objeto InkCollector a ela e fornece ao usuário opções de menu que podem ser usadas para alterar a cor da tinta, a largura da tinta e habilitar e desabilitar a coleta de tinta.

> [!Note]  
> a versão discutida nesta seção é Visual Basic .net. Os conceitos são os mesmos entre outras versões de idioma na biblioteca de exemplos.

 

## <a name="declaring-the-inkcollector"></a>Declarando o InkCollector

Primeiro, o aplicativo importa o namespace [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) . Em seguida, o aplicativo declara `myInkCollector` , que contém o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) do formulário.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Configurando as coisas

O método do formulário `InkCollection_Load` manipula o evento de [carregamento](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário. Ele cria um objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) atribuído ao formulário que modifica a propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto InkCollector e habilita o objeto InkCollector.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



O [InkCollector](/previous-versions/ms836493(v=msdn.10)) é atribuído à janela do formulário atribuindo o identificador de janela do formulário à propriedade [Handle](/previous-versions/ms836504(v=msdn.10)) do objeto InkCollector. A coleta de tinta é ativada definindo a propriedade [habilitada](/previous-versions/ms836503(v=msdn.10)) do objeto InkCollector como **true**.

A propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) define os atributos padrão que são atribuídos a um novo cursor. Para definir atributos diferentes em um novo cursor, use a propriedade [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) do objeto [cursor](/previous-versions/ms839521(v=msdn.10)) . Para alterar os atributos de desenho de um único traço, use a propriedade [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .

## <a name="changing-the-properties"></a>Alterando as propriedades

O restante desse aplicativo simples consiste em manipuladores para as várias seleções de menu que o usuário pode fazer. Por exemplo, quando o usuário escolhe alterar a cor da tinta para vermelho selecionando vermelho no menu de tinta, a cor é alterada usando a propriedade [Color](/previous-versions/ms837933(v=msdn.10)) na propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) no manipulador de eventos do menu.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
