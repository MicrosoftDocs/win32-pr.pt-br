---
title: IAgentCharacter getociosidade
description: IAgentCharacter getociosidade
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637266"
---
# <a name="iagentcharactergetidleon"></a><span data-ttu-id="9761d-103">IAgentCharacter:: getidley</span><span class="sxs-lookup"><span data-stu-id="9761d-103">IAgentCharacter::GetIdleOn</span></span>

<span data-ttu-id="9761d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9761d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

<span data-ttu-id="9761d-105">Indica o estado de processamento de ociosidade automático para um caractere.</span><span class="sxs-lookup"><span data-stu-id="9761d-105">Indicates the automatic idle processing state for a character.</span></span>

-   <span data-ttu-id="9761d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9761d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9761d-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="9761d-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="9761d-108">Endereço de uma variável que recebe **true** se o servidor do Microsoft Agent reproduzir automaticamente animações de estado **deixar** para um caractere e **false** se não.</span><span class="sxs-lookup"><span data-stu-id="9761d-108">Address of a variable that receives **True** if the Microsoft Agent server automatically plays **Idling** state animations for a character and **False** if not.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="9761d-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9761d-109">See Also</span></span>

[<span data-ttu-id="9761d-110">**IAgentCharacter:: setidleion**</span><span class="sxs-lookup"><span data-stu-id="9761d-110">**IAgentCharacter::SetIdleOn**</span></span>](iagentcharacter--setidleon.md)


 

 




