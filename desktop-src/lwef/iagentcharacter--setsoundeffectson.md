---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798474"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="9c270-103">IAgentCharacter::SetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="9c270-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="9c270-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9c270-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="9c270-105">Determina se os efeitos de som do caractere são reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="9c270-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="9c270-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9c270-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9c270-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bno*</span><span class="sxs-lookup"><span data-stu-id="9c270-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="9c270-108">Configuração de efeitos de som.</span><span class="sxs-lookup"><span data-stu-id="9c270-108">Sound effects setting.</span></span> <span data-ttu-id="9c270-109">Se esse parâmetro for **true**, os efeitos de som das animações serão reproduzidos quando a animação for reproduzida; Se **for false**, os efeitos sonoros não serão reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="9c270-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="9c270-110">Essa configuração determina se os efeitos sonoros compilados como parte do caractere são reproduzidos quando você executa uma animação associada.</span><span class="sxs-lookup"><span data-stu-id="9c270-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="9c270-111">A configuração dessa propriedade se aplica a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="9c270-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="9c270-112">A configuração também está sujeita à configuração de efeitos de som global do usuário em [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="9c270-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9c270-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="9c270-113">See Also</span></span>

<span data-ttu-id="9c270-114">[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="9c270-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




