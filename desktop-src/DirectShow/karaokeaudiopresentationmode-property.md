---
description: A propriedade KaraokeAudioPresentationMode define ou recupera a combinação de alto-falantes à esquerda para os canais auxiliares do karaokê.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propriedade KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810935"
---
# <a name="karaokeaudiopresentationmode-property"></a>Propriedade KaraokeAudioPresentationMode

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `KaraokeAudioPresentationMode` propriedade define ou recupera a combinação de alto-falantes à direita para os canais do karaokê auxiliar.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que contém um conjunto de sinalizadores de bit indicando como os canais auxiliares do karaokê são downmixeds aos alto-falantes esquerdo e direito.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de zero.

Os canais de áudio são baseados em zero, de modo que os canais 0 e 1 geralmente representam os canais do alto-falante direito e esquerdo e os canais 2 a 4 são os três canais auxiliares do karaokê. Quando o objeto MSWebDVD entra no modo karaokê, ele automaticamente desativa os canais 2 e superiores. Use operações **or bits para** definir o bit apropriado para enviar um canal auxiliar para o palestrante esquerdo, o orador direito, ambos os alto-falantes (ambos os bits) ou para nenhum alto-falante (ambos bits desativados). Esses bits são todos desativados por padrão sempre que o navegador de DVD entra no modo de karaokê. O valor dos bits e sua ação correspondente são fornecidos na tabela a seguir.



| Valor  | Descrição                            |
|--------|----------------------------------------|
| 0x0004 | Canal 2 do downmix para o alto-falante esquerdo  |
| 0x0008 | Downmix canal 3 para o alto-falante esquerdo  |
| 0x0010 | Canal 4 do downmix para o alto-falante esquerdo  |
| 0x0400 | Downmix canal 2 para o alto-falante direito |
| 0x0800 | Downmix Channel 3 para o alto-falante direito |
| 0x1000 | Canal 4 do downmix para o alto-falante direito |



 

 

 



