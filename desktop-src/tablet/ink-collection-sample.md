---
description: Esse aplicativo é baseado no objeto InkCollector e demonstra a coleta de tinta.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Exemplo de coleção de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090294"
---
# <a name="ink-collection-sample"></a><span data-ttu-id="f3ff0-103">Exemplo de coleção de tinta</span><span class="sxs-lookup"><span data-stu-id="f3ff0-103">Ink Collection Sample</span></span>

<span data-ttu-id="f3ff0-104">Esse aplicativo é baseado no objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) e demonstra a coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="f3ff0-105">O aplicativo cria uma janela, anexa um objeto InkCollector a ela e fornece ao usuário opções de menu que podem ser usadas para alterar a cor da tinta, a largura da tinta e habilitar e desabilitar a coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="f3ff0-106">A versão discutida nesta seção é Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="f3ff0-107">Os conceitos são os mesmos entre outras versões de idioma na biblioteca de exemplos.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="f3ff0-108">Declarando o InkCollector</span><span class="sxs-lookup"><span data-stu-id="f3ff0-108">Declaring the InkCollector</span></span>

<span data-ttu-id="f3ff0-109">Primeiro, o aplicativo importa o namespace [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3ff0-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="f3ff0-110">Em seguida, o aplicativo declara `myInkCollector` , que contém o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) do formulário.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="f3ff0-111">Configurando as coisas</span><span class="sxs-lookup"><span data-stu-id="f3ff0-111">Setting Things Up</span></span>

<span data-ttu-id="f3ff0-112">O método do formulário `InkCollection_Load` manipula o evento de [carregamento](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="f3ff0-113">Ele cria um objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) atribuído ao formulário que modifica a propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto InkCollector e habilita o objeto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


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



<span data-ttu-id="f3ff0-114">O [InkCollector](/previous-versions/ms836493(v=msdn.10)) é atribuído à janela do formulário atribuindo o identificador de janela do formulário à propriedade [Handle](/previous-versions/ms836504(v=msdn.10)) do objeto InkCollector.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="f3ff0-115">A coleta de tinta é ativada definindo a propriedade [habilitada](/previous-versions/ms836503(v=msdn.10)) do objeto InkCollector como **true**.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="f3ff0-116">A propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) define os atributos padrão que são atribuídos a um novo cursor.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="f3ff0-117">Para definir atributos diferentes em um novo cursor, use a propriedade [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) do objeto [cursor](/previous-versions/ms839521(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3ff0-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="f3ff0-118">Para alterar os atributos de desenho de um único traço, use a propriedade [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f3ff0-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="f3ff0-119">Alterando as propriedades</span><span class="sxs-lookup"><span data-stu-id="f3ff0-119">Changing the Properties</span></span>

<span data-ttu-id="f3ff0-120">O restante desse aplicativo simples consiste em manipuladores para as várias seleções de menu que o usuário pode fazer.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="f3ff0-121">Por exemplo, quando o usuário escolhe alterar a cor da tinta para vermelho selecionando vermelho no menu de tinta, a cor é alterada usando a propriedade [Color](/previous-versions/ms837933(v=msdn.10)) na propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) no manipulador de eventos do menu.</span><span class="sxs-lookup"><span data-stu-id="f3ff0-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="f3ff0-122">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="f3ff0-122">Closing the Form</span></span>

<span data-ttu-id="f3ff0-123">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="f3ff0-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
