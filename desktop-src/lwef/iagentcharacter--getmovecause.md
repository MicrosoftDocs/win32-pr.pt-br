---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119672"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="a281a-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="a281a-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="a281a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a281a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="a281a-105">Recupera a causa da última movimentação do caractere.</span><span class="sxs-lookup"><span data-stu-id="a281a-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="a281a-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a281a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a281a-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="a281a-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="a281a-108">Endereço de uma variável que recebe a causa da última movimentação do caractere e será um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="a281a-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="a281a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a281a-109">Value</span></span>                                                               | <span data-ttu-id="a281a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a281a-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a281a-111">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="a281a-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="a281a-112">O caractere não foi movido.</span><span class="sxs-lookup"><span data-stu-id="a281a-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="a281a-113">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="a281a-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="a281a-114">O usuário arrastou o caractere.</span><span class="sxs-lookup"><span data-stu-id="a281a-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="a281a-115">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="a281a-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="a281a-116">Seu aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="a281a-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="a281a-117">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="a281a-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="a281a-118">Outro aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="a281a-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="a281a-119">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="a281a-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="a281a-120">O servidor moveu o caractere para mantê-lo na tela após uma alteração na resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="a281a-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a281a-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a281a-121">See Also</span></span>

[<span data-ttu-id="a281a-122">**IAgentNotifySink::Move**</span><span class="sxs-lookup"><span data-stu-id="a281a-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





