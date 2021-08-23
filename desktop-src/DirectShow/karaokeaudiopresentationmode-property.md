---
description: A propriedade LtdeAudioPresentationMode define ou recupera a combinação de alto-falantes à direita para os canais auxiliares.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Propriedade LtdeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af634a3beaade7e497cdc6d158ccf1121ebb09542bdec92ceaae823b1b91ccdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952375"
---
# <a name="karaokeaudiopresentationmode-property"></a>Propriedade LtdeAudioPresentationMode

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `KaraokeAudioPresentationMode` propriedade define ou recupera a combinação de alto-falantes à direita para os canais auxiliares.

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que contém um conjunto de sinalizadores de bits que indicam como os canais auxiliares são desmixados para os alto-falantes esquerdo e direito.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de zero.

Os canais de áudio são baseados em zero, portanto, os canais 0 e 1 geralmente representam os canais do locutor direito e esquerdo e os canais 2 a 4 são os três canais auxiliares. Quando o objeto MSWebDVD entra no modo DevVD, ele muda automaticamente os canais 2 e superior. Use operações **OR** bit a bit para definir o bit apropriado para enviar um canal auxiliar para o locutor esquerdo, o alto-falante direito, ambos os alto-falantes (ambos os bits) ou para nenhum alto-falante (ambos os bits desligados). Esses bits são todos desligados por padrão sempre que o Navegador de DVD entra no modo de gravação. O valor dos bits e sua ação correspondente é dado na tabela a seguir.



| Valor  | Descrição                            |
|--------|----------------------------------------|
| 0x0004 | Downmix Channel 2 para o alto-falante esquerdo  |
| 0x0008 | Downmix Channel 3 para o alto-falante esquerdo  |
| 0x0010 | Downmix Channel 4 para o alto-falante esquerdo  |
| 0x0400 | Downmix Channel 2 para o alto-falante direito |
| 0x0800 | Downmix Channel 3 para o alto-falante direito |
| 0x1000 | Downmix Channel 4 para o alto-falante direito |



 

 

 



