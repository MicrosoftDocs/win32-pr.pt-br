---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781492"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="9bc4f-103">IAgentCharacter::GetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="9bc4f-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="9bc4f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9bc4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="9bc4f-105">Recupera se a configuração de efeitos de som do caractere está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="9bc4f-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9bc4f-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="9bc4f-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="9bc4f-108">Endereço de uma variável que recebe **true** se a configuração de efeitos de som do caractere estiver habilitada; **false** se estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="9bc4f-109">A configuração de efeitos de som do caractere determina se os efeitos sonoros compilados como parte do caractere são reproduzidos quando você executa uma animação associada.</span><span class="sxs-lookup"><span data-stu-id="9bc4f-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="9bc4f-110">A configuração está sujeita à configuração de efeitos de som global do usuário em [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="9bc4f-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9bc4f-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9bc4f-111">See Also</span></span>

<span data-ttu-id="9bc4f-112">[**IAgentCharacter:: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="9bc4f-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




