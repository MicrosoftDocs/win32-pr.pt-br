---
title: GetVersion do IAgentEx
description: GetVersion do IAgentEx
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292403"
---
# <a name="iagentexgetversion"></a><span data-ttu-id="c9b2e-103">IAgentEx:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="c9b2e-103">IAgentEx::GetVersion</span></span>

<span data-ttu-id="c9b2e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c9b2e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="c9b2e-105">Recupera o número de versão do servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c9b2e-105">Retrieves the version number of Microsoft Agent server.</span></span>

-   <span data-ttu-id="c9b2e-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c9b2e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c9b2e-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span><span class="sxs-lookup"><span data-stu-id="c9b2e-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="c9b2e-108">Endereço de uma variável que recebe a versão principal.</span><span class="sxs-lookup"><span data-stu-id="c9b2e-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="c9b2e-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span><span class="sxs-lookup"><span data-stu-id="c9b2e-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="c9b2e-110">Endereço de uma variável que recebe a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="c9b2e-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

 

 




