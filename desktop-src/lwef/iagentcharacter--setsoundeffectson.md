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
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Determina se os efeitos de som do caractere são reproduzidos.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bno*
</dt> <dd>

Configuração de efeitos de som. Se esse parâmetro for **true**, os efeitos de som das animações serão reproduzidos quando a animação for reproduzida; Se **for false**, os efeitos sonoros não serão reproduzidos.

</dd> </dl>

Essa configuração determina se os efeitos sonoros compilados como parte do caractere são reproduzidos quando você executa uma animação associada. A configuração dessa propriedade se aplica a todos os clientes do caractere. A configuração também está sujeita à configuração de efeitos de som global do usuário em [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




