---
description: A propriedade volume define ou recupera o volume do alto-falante para a saída do fluxo de áudio.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Propriedade Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502240"
---
# <a name="volume-property"></a>Propriedade Volume

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `Volume` propriedade define ou recupera o volume do alto-falante para a saída do fluxo de áudio.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Valor Retornado

Retorna o nível de volume como atenuação em decibéis como um inteiro.

## <a name="remarks"></a>Comentários

Essa propriedade é de leitura/gravação com um valor padrão de 0. O volume completo é 0 e 10.000 é silêncio; a escala é logarítmica. Multiplique o nível de decibéi desejado por 100 (por exemplo, 10.000 = 100 dB).

 

 



