---
description: A propriedade VolumesAvailable recupera o número de volumes em um conjunto de vários volumes.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propriedade VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0ab5b07f30e49f1bbe7655a2d66d9aaa683099df64cadf94b5dfffdd3b3af0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650933"
---
# <a name="volumesavailable-property"></a>Propriedade VolumesAvailable

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `VolumesAvailable` propriedade recupera o número de volumes em um conjunto de vários volumes.

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a>Valor Retornado

Retorna o número de volumes no conjunto como um inteiro.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. Alguns títulos de DVD podem ser lançados como um conjunto ou série de vários discos. Use esse método para determinar o número de volume do disco atual.

 

 



