---
description: Esse evento é publicado pelo controle ScrollableText para permitir que o usuário imprima o conteúdo desse controle.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837202"
---
# <a name="msiprint-controlevent"></a><span data-ttu-id="cfe03-103">MsiPrint ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="cfe03-103">MsiPrint ControlEvent</span></span>

<span data-ttu-id="cfe03-104">Esse evento é publicado pelo [controle ScrollableText](scrollabletext-control.md) para permitir que o usuário imprima o conteúdo desse controle.</span><span class="sxs-lookup"><span data-stu-id="cfe03-104">This event is published by the [ScrollableText Control](scrollabletext-control.md) to enable the user to print the contents of that control.</span></span>

<span data-ttu-id="cfe03-105">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="cfe03-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="cfe03-106">Esse ControlEvent, está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="cfe03-106">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="cfe03-107">Esse evento deve ser assinado por um controle de [pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o [controle ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="cfe03-107">This event should be subscribed to by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the [ScrollableText Control](scrollabletext-control.md).</span></span> <span data-ttu-id="cfe03-108">TheMsiPrint ControlEvent, deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="cfe03-108">TheMsiPrint ControlEvent should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="cfe03-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="cfe03-109">Published By</span></span>

[<span data-ttu-id="cfe03-110">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="cfe03-110">ScrollableText</span></span>](scrollabletext-control.md)

## <a name="argument"></a><span data-ttu-id="cfe03-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="cfe03-111">Argument</span></span>

<span data-ttu-id="cfe03-112">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="cfe03-112">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="cfe03-113">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="cfe03-113">Action on Subscribers</span></span>

<span data-ttu-id="cfe03-114">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="cfe03-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="cfe03-115">Usos comum</span><span class="sxs-lookup"><span data-stu-id="cfe03-115">Typical Use</span></span>

<span data-ttu-id="cfe03-116">Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo que o [controle ScrollableText](scrollabletext-control.md) pode ser usado para exibir uma caixa de diálogo modal, permitindo que o usuário imprima o conteúdo do controle ScrollableText.</span><span class="sxs-lookup"><span data-stu-id="cfe03-116">A [PushButton](pushbutton-control.md) control on the same dialog box as the [ScrollableText Control](scrollabletext-control.md) can be used to display a modal dialog box enabling the user to print the contents of the ScrollableText Control.</span></span>

 

 



