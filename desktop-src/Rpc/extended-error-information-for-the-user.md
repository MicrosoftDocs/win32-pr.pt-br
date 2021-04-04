---
title: Informações de erro estendidas para o usuário
description: Se informações de erro estendidas estiverem disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a localização do problema.
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822711"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="43287-103">Informações de erro estendidas para o usuário</span><span class="sxs-lookup"><span data-stu-id="43287-103">Extended Error Information for the User</span></span>

<span data-ttu-id="43287-104">Se informações de erro estendidas estiverem disponíveis, os componentes que participam da criação das informações de erro estendidas devem facilitar a localização do problema.</span><span class="sxs-lookup"><span data-stu-id="43287-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="43287-105">A primeira etapa é examinar o último registro de erro estendido e determinar em qual computador e qual processo o problema foi originado.</span><span class="sxs-lookup"><span data-stu-id="43287-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="43287-106">Isso é geralmente a causa do erro de RPC \_ S \_ \* .</span><span class="sxs-lookup"><span data-stu-id="43287-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="43287-107">Localize o local de detecção e determine quais são os parâmetros para esse local de detecção.</span><span class="sxs-lookup"><span data-stu-id="43287-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="43287-108">Normalmente, eles indicam uma falha de uma chamada de função ou de uma verificação específica.</span><span class="sxs-lookup"><span data-stu-id="43287-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="43287-109">A partir daí, determine por que a função ou verificação falha e execute uma ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="43287-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="43287-110">Os registros antes do último registro indicam o caminho pelo qual o erro chegou e geralmente servem como uma verificação de sanidade, em vez de um auxílio no processo de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="43287-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




