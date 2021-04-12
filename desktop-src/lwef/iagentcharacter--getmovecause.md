---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364504"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="8555f-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="8555f-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="8555f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8555f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="8555f-105">Recupera a causa da última movimentação do caractere.</span><span class="sxs-lookup"><span data-stu-id="8555f-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="8555f-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8555f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8555f-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="8555f-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8555f-108">Endereço de uma variável que recebe a causa da última movimentação do caractere e será um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="8555f-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8555f-109">**const NeverMoved curto não assinado** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="8555f-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="8555f-110">O caractere não foi movido.</span><span class="sxs-lookup"><span data-stu-id="8555f-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="8555f-111">**const não assinada curto-** **movida = 1;**</span><span class="sxs-lookup"><span data-stu-id="8555f-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="8555f-112">O usuário arrastou o caractere.</span><span class="sxs-lookup"><span data-stu-id="8555f-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="8555f-113">**const ProgramMoved curto não assinado** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="8555f-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="8555f-114">Seu aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="8555f-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="8555f-115">**const OtherProgramMoved curto não assinado** **= 3;**</span><span class="sxs-lookup"><span data-stu-id="8555f-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="8555f-116">Outro aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="8555f-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="8555f-117">**const SystemMoved curto sem sinal** **= 4**</span><span class="sxs-lookup"><span data-stu-id="8555f-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="8555f-118">O servidor moveu o caractere para mantê-lo na tela após uma alteração de resolução de tela.</span><span class="sxs-lookup"><span data-stu-id="8555f-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8555f-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8555f-119">See Also</span></span>

[<span data-ttu-id="8555f-120">**IAgentNotifySink:: mover**</span><span class="sxs-lookup"><span data-stu-id="8555f-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





