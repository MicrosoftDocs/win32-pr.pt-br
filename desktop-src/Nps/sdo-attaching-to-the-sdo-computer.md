---
title: Anexando ao computador SDO
description: Com o ponteiro de interface retornado por CoCreateInstance, chame o método ISdoMachine Attach.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917379"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="388ae-103">Anexando ao computador SDO</span><span class="sxs-lookup"><span data-stu-id="388ae-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="388ae-104">Com o ponteiro de interface retornado por [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), chame o método [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) .</span><span class="sxs-lookup"><span data-stu-id="388ae-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="388ae-105">Passe **NULL** como o parâmetro para o método **Attach** .</span><span class="sxs-lookup"><span data-stu-id="388ae-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="388ae-106">O valor **NULL** especifica que **Attach** associa o objeto de computador ao computador local.</span><span class="sxs-lookup"><span data-stu-id="388ae-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="388ae-107">Não há suporte para a anexação a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="388ae-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="388ae-108">Para determinar se o computador local já está anexado, chame o método [**ISdoMachine:: GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) .</span><span class="sxs-lookup"><span data-stu-id="388ae-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="388ae-109">Consulte [anexando a um computador SDO-Enabled](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) para ver o código de exemplo que demonstra como anexar ao computador local.</span><span class="sxs-lookup"><span data-stu-id="388ae-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 