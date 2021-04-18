---
description: Visão geral da exibição do painel de entrada.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Exibindo o painel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782423"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="2d3e8-103">Exibindo o painel de entrada</span><span class="sxs-lookup"><span data-stu-id="2d3e8-103">Displaying the Input Panel</span></span>

<span data-ttu-id="2d3e8-104">\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) para código gerenciado).</span><span class="sxs-lookup"><span data-stu-id="2d3e8-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="2d3e8-105">Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="2d3e8-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="2d3e8-106">A ordem dos vários eventos de foco de um controle é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d3e8-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="2d3e8-107">Controle. Enter</span><span class="sxs-lookup"><span data-stu-id="2d3e8-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="2d3e8-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="2d3e8-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="2d3e8-109">Controle. Leave</span><span class="sxs-lookup"><span data-stu-id="2d3e8-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="2d3e8-110">Controle. Validating</span><span class="sxs-lookup"><span data-stu-id="2d3e8-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="2d3e8-111">Controle. validado</span><span class="sxs-lookup"><span data-stu-id="2d3e8-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="2d3e8-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="2d3e8-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="2d3e8-113">Não há nenhuma garantia de que o controle realmente tem o foco no momento em que a propriedade [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) é gravada quando é definida no manipulador de eventos [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="2d3e8-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="2d3e8-114">O evento Control. Enter é o melhor lugar para anexar o objeto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a um controle, mas o evento [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) é o melhor local para alterar a propriedade [PenInputPanel. Visible](/previous-versions/ms571984(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="2d3e8-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
