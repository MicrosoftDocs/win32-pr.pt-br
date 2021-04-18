---
description: Use controles padrão do Windows sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft. Isso inclui controles fornecidos pelo Windows (User32.dll) e pela biblioteca de controles comuns do Windows (Comctl32.dll).
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Usando controles padrão do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296306"
---
# <a name="using-standard-windows-controls"></a><span data-ttu-id="a394f-104">Usando controles padrão do Windows</span><span class="sxs-lookup"><span data-stu-id="a394f-104">Using Standard Windows Controls</span></span>

<span data-ttu-id="a394f-105">Use controles padrão do Windows sempre que possível, pois eles são totalmente compatíveis com as diretrizes de Acessibilidade Ativa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a394f-105">Use standard Windows controls whenever possible, because they are fully compatible with Microsoft Active Accessibility guidelines.</span></span> <span data-ttu-id="a394f-106">Isso inclui controles fornecidos pelo Windows (User32.dll) e pela biblioteca de controles comuns do Windows (Comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="a394f-106">This includes controls provided by Windows (User32.dll) and the Windows common controls library (Comctl32.dll).</span></span>

<span data-ttu-id="a394f-107">Cada controle padrão do Windows é uma janela separada de uma classe específica, portanto, o auxílio de acessibilidade é notificado quando o foco é movido para um novo controle.</span><span class="sxs-lookup"><span data-stu-id="a394f-107">Each standard Windows control is a separate window of a specific class, so the accessibility aid is notified when the focus moves to a new control.</span></span> <span data-ttu-id="a394f-108">O auxílio pode determinar a classe da janela de controles e todas as mensagens adicionais que ele pode enviar para consultar ou alterar o estado dos controles.</span><span class="sxs-lookup"><span data-stu-id="a394f-108">The aid can determine the controls window class, and any additional messages it can send to query or alter the controls state.</span></span> <span data-ttu-id="a394f-109">O auxílio também pode identificar todos os controles filho contidos em uma janela pai e identificar o pai de qualquer controle.</span><span class="sxs-lookup"><span data-stu-id="a394f-109">The aid can also identify all of the child controls contained within a parent window and identify the parent of any control.</span></span>

<span data-ttu-id="a394f-110">Alguns controles comuns são extremamente flexíveis e, muitas vezes, podem substituir controles personalizados menos acessíveis e controles desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="a394f-110">Some common controls are extremely flexible and can often substitute for less-accessible custom controls and owner-drawn controls.</span></span> <span data-ttu-id="a394f-111">Por exemplo, um modo de exibição de lista pode substituir uma caixa de listagem desenhada pelo proprietário para exibir uma caixa de seleção ao lado de cada item.</span><span class="sxs-lookup"><span data-stu-id="a394f-111">For example, a list view can replace an owner-drawn list box to display a check box next to each item.</span></span> <span data-ttu-id="a394f-112">Como outro exemplo, o controle de botão avançado pode exibir imagens e texto.</span><span class="sxs-lookup"><span data-stu-id="a394f-112">As another example, the enhanced button control can display both images and text.</span></span> <span data-ttu-id="a394f-113">Anteriormente, isso exigia o uso de um controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="a394f-113">Previously, this required the use of a custom control.</span></span>

 

 



