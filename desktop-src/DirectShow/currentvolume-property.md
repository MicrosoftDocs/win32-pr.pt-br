---
description: A propriedade CurrentVolume recupera o número de volume para o diretório raiz atual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriedade CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d07f9d82facc243654bad2e16e9a028e8cf920a51f15dd92cc879b0ea1340d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654597"
---
# <a name="currentvolume-property"></a>Propriedade CurrentVolume

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentVolume` propriedade recupera o número de volume para o diretório raiz atual.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o volume de DVD atual. Se um disco faz parte de um conjunto de vários volumes, o valor inteiro deve ser maior que zero.

## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura sem valor padrão.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



