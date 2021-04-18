---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105815416"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="37c97-103">IAgentCharacter:: SetName</span><span class="sxs-lookup"><span data-stu-id="37c97-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="37c97-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37c97-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="37c97-105">Define o nome do caractere.</span><span class="sxs-lookup"><span data-stu-id="37c97-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="37c97-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="37c97-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="37c97-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="37c97-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="37c97-108">Um BSTR que define o nome do caractere.</span><span class="sxs-lookup"><span data-stu-id="37c97-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="37c97-109">O nome padrão de um caractere é definido quando ele é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="37c97-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="37c97-110">Você pode alterá-lo usando **IAgentCharacter:: SetName**; no entanto, isso altera o nome do caractere para todos os clientes atuais do caractere.</span><span class="sxs-lookup"><span data-stu-id="37c97-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="37c97-111">Essa propriedade não é persistente (armazenada permanentemente).</span><span class="sxs-lookup"><span data-stu-id="37c97-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="37c97-112">O nome do caractere é revertido para seu nome padrão sempre que o caractere é carregado pela primeira vez por um cliente.</span><span class="sxs-lookup"><span data-stu-id="37c97-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="37c97-113">O nome do caractere também pode depender de sua ID de idioma.</span><span class="sxs-lookup"><span data-stu-id="37c97-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="37c97-114">Os caracteres podem ser compilados com nomes diferentes para idiomas diferentes.</span><span class="sxs-lookup"><span data-stu-id="37c97-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="37c97-115">O servidor usa a configuração de nome do caractere em partes da interface do Microsoft Agent, como o título da janela de comandos de voz quando o caractere é entrada-ativo e no menu pop-up da barra de tarefas do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="37c97-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="37c97-116">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="37c97-116">See Also</span></span>

[<span data-ttu-id="37c97-117">**IAgentCharacter:: GetName**</span><span class="sxs-lookup"><span data-stu-id="37c97-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




