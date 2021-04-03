---
title: IAgentCharacter getVisible
description: IAgentCharacter getVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084466"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="5d65c-103">IAgentCharacter:: getVisible</span><span class="sxs-lookup"><span data-stu-id="5d65c-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="5d65c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d65c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="5d65c-105">Determina se o quadro de animação do caractere está visível no momento.</span><span class="sxs-lookup"><span data-stu-id="5d65c-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="5d65c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5d65c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5d65c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="5d65c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="5d65c-108">Endereço de uma variável que recebe **true** se o quadro do caractere estiver visível e **false** se estiver oculto.</span><span class="sxs-lookup"><span data-stu-id="5d65c-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="5d65c-109">Você pode usar esse método para determinar se o quadro do caractere está visível no momento.</span><span class="sxs-lookup"><span data-stu-id="5d65c-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="5d65c-110">Para tornar um caractere visível, use o método [**show**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="5d65c-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="5d65c-111">Para ocultar um caractere, use o método [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .</span><span class="sxs-lookup"><span data-stu-id="5d65c-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 