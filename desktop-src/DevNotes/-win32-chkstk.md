---
description: Chamado pelo compilador quando você tem mais de uma página de variáveis locais em sua função.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: Rotina de _chkstk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920108"
---
# <a name="_chkstk-routine"></a><span data-ttu-id="a7ba9-103">\_Rotina chkstk</span><span class="sxs-lookup"><span data-stu-id="a7ba9-103">\_chkstk Routine</span></span>

<span data-ttu-id="a7ba9-104">Chamado pelo compilador quando você tem mais de uma página de variáveis locais em sua função.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-104">Called by the compiler when you have more than one page of local variables in your function.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7ba9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7ba9-105">Remarks</span></span>

<span data-ttu-id="a7ba9-106">\_a rotina chkstk é uma rotina auxiliar para o compilador C.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-106">\_chkstk Routine is a helper routine for the C compiler.</span></span> <span data-ttu-id="a7ba9-107">Para compiladores x86, \_ a rotina chkstk é chamada quando as variáveis locais excedem 4K bytes; para compiladores x64, ele é 8K.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-107">For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.</span></span>

 

 



