---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725016"
---
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




