---
description: Um processo pode chamar WSPCloseSocket em um soquete duplicado e o descritor ficará desalocado. No entanto, o soquete subjacente permanecerá aberto até que WSPCloseSocket seja chamado no último descritor restante.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Contagem de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788896"
---
# <a name="reference-counting"></a><span data-ttu-id="c5da2-104">Contagem de referência</span><span class="sxs-lookup"><span data-stu-id="c5da2-104">Reference Counting</span></span>

<span data-ttu-id="c5da2-105">Um processo pode chamar [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) em um soquete duplicado e o descritor ficará desalocado.</span><span class="sxs-lookup"><span data-stu-id="c5da2-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="c5da2-106">No entanto, o soquete subjacente permanecerá aberto até que **WSPCloseSocket** seja chamado no último descritor restante.</span><span class="sxs-lookup"><span data-stu-id="c5da2-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
