---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814075"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="acfb4-103">IAgentNotifySinkEx::D efaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="acfb4-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="acfb4-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="acfb4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="acfb4-105">Notifica um aplicativo cliente quando o caractere padrão é alterado.</span><span class="sxs-lookup"><span data-stu-id="acfb4-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="acfb4-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="acfb4-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="acfb4-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span><span class="sxs-lookup"><span data-stu-id="acfb4-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="acfb4-108">O identificador exclusivo do caractere.</span><span class="sxs-lookup"><span data-stu-id="acfb4-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="acfb4-109">Quando o usuário altera o caractere atribuído como o caractere padrão do usuário, o servidor envia esse evento aos clientes que carregaram o caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="acfb4-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="acfb4-110">O evento retorna o GUID (identificador exclusivo) do caractere formatado com chaves e traços, que é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="acfb4-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="acfb4-111">Quando o novo caractere é exibido, ele assume o mesmo tamanho que qualquer instância já carregada do caractere ou o caractere padrão anterior (nessa ordem).</span><span class="sxs-lookup"><span data-stu-id="acfb4-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="acfb4-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="acfb4-112">See Also</span></span>

[<span data-ttu-id="acfb4-113">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="acfb4-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




