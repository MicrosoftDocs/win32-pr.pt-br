---
description: Descreve como criar um objeto PenInputPanel.
ms.assetid: fd9ce912-5cec-4bec-b7d8-5a4f71000c95
title: Criando um objeto PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072d5dca28801ee45b7747504a93d755443cfb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781429"
---
# <a name="creating-a-peninputpanel-object"></a><span data-ttu-id="815b8-103">Criando um objeto PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="815b8-103">Creating a PenInputPanel Object</span></span>

<span data-ttu-id="815b8-104">\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) e [Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="815b8-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) and [Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)).</span></span> <span data-ttu-id="815b8-105">Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="815b8-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="815b8-106">Os construtores de código gerenciado fornecem uma maneira conveniente de criar um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) e anexá-lo a um controle em uma única etapa.</span><span class="sxs-lookup"><span data-stu-id="815b8-106">Managed code constructors provide a convenient way to create a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object and attach it to a control in one step.</span></span> <span data-ttu-id="815b8-107">Este \# exemplo C cria um objeto PenInputPanel e o anexa a um controle [InkEdit](/previous-versions/ms835842(v=msdn.10)) existente, `InkEdit1` com uma linha de código.</span><span class="sxs-lookup"><span data-stu-id="815b8-107">This C\# example creates a PenInputPanel object and attaches it to an existing [InkEdit](/previous-versions/ms835842(v=msdn.10)) control, `InkEdit1`, with one line of code.</span></span>


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(InkEdit1);
```



<span data-ttu-id="815b8-108">O mesmo exemplo em Visual Basic .NET tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="815b8-108">The same example in Visual Basic .NET looks like this:</span></span>


```C++
Dim thePenInputPanel As New PenInputPanel(InkEdit1)
```



<span data-ttu-id="815b8-109">Essa técnica é útil em casos em que um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) será associado a um único controle durante seu tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="815b8-109">This technique is useful in cases where one [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object will be associated with a single control throughout its lifetime.</span></span> <span data-ttu-id="815b8-110">Nos casos em que você deseja usar um objeto PenInputPanel e associá-lo a vários controles, como demonstrado no [exemplo de PenInputPanel](peninputpanel-sample.md), use a propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) para alterar o controle ao qual o objeto PenInputPanel está associado.</span><span class="sxs-lookup"><span data-stu-id="815b8-110">In cases where you want to use one PenInputPanel object and associate it with multiple controls, as demonstrated in the [PenInputPanel Sample](peninputpanel-sample.md), use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property to change the control to which the PenInputPanel object is associated.</span></span>

<span data-ttu-id="815b8-111">Para anexar um objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a um controle sem usar um construtor, use a propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="815b8-111">To attach a [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control without using a constructor, use the [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) property.</span></span> <span data-ttu-id="815b8-112">Use essa técnica para idiomas que não dão suporte aos construtores gerenciados, como C++.</span><span class="sxs-lookup"><span data-stu-id="815b8-112">Use this technique for languages that do not support the managed constructors, such as C++.</span></span>

 

 
