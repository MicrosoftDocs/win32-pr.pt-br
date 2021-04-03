---
description: Esse atributo especifica se os arquivos de backup de reversão são incluídos nos custos exibidos pelo controle VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Atributo de controle ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829478"
---
# <a name="controlshowrollbackcost-control-attribute"></a>Atributo de controle ControlShowRollbackCost

Esse atributo especifica se os arquivos de backup de reversão são incluídos nos custos exibidos pelo [controle VolumeCostList](volumecostlist-control.md).

Se esse bit for definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de reversão serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).

Se esse bit não for definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de reversão não serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controles válidos

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Comentários

Esse atributo de controle será ignorado se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou F.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, o custo da reversão, os arquivos de backup serão incluídos.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou [**DISABLEROLLBACK**](-disablerollback.md) Propriedade = 1, o custo da reversão, os arquivos de backup não serão incluídos.

 

 



