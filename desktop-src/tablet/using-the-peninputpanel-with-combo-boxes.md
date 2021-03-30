---
description: Descreve como usar o objeto PenInputPanel com caixas de combinação.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Usando o PenInputPanel com caixas de combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647090"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="2e79c-103">Usando o PenInputPanel com caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="2e79c-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="2e79c-104">\[O objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) foi substituído por [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="2e79c-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="2e79c-105">Consulte a [programação do painel de entrada de texto](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="2e79c-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="2e79c-106">Se você anexar um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) a um controle [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) , em seguida, toque na caneta do Tablet na caixa de combinação editar parte do controle em tempo de execução, o objeto PenInputPanel não será exibido.</span><span class="sxs-lookup"><span data-stu-id="2e79c-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="2e79c-107">No entanto, ela será exibida se você tocar na seta suspensa.</span><span class="sxs-lookup"><span data-stu-id="2e79c-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="2e79c-108">Isso ocorre porque a janela do controle de edição na caixa de combinação não é a janela que recebe mensagens de caneta.</span><span class="sxs-lookup"><span data-stu-id="2e79c-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="2e79c-109">As caixas de combinação têm uma janela de edição filho.</span><span class="sxs-lookup"><span data-stu-id="2e79c-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="2e79c-110">A solução para esse problema é determinar se a janela à qual o objeto PenInputPanel está anexado tem uma janela filho.</span><span class="sxs-lookup"><span data-stu-id="2e79c-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="2e79c-111">Nesse caso, você pode anexar o objeto PenInputPanel à janela filho.</span><span class="sxs-lookup"><span data-stu-id="2e79c-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="2e79c-112">Definir a propriedade [VerticalOffset](/previous-versions/ms571983(v=vs.100)) do objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) como um valor de-1 faz com que o painel apareça na parte superior da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="2e79c-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 
