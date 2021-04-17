---
description: A propriedade CurrentVolume recupera o número de volume para o diretório raiz atual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propriedade CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789649"
---
# <a name="currentvolume-property"></a>Propriedade CurrentVolume

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentVolume` propriedade recupera o número de volume para o diretório raiz atual.

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o volume de DVD atual. Se um disco fizer parte de um conjunto de vários volumes, o valor inteiro deverá ser maior que zero.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**VolumesAvailable**](volumesavailable-property.md)
</dt> </dl>

 

 



