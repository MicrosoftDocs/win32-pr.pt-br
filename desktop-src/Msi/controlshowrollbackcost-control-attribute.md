---
description: Esse atributo especifica se os arquivos de backup de redução estão incluídos ou não nos custos exibidos pelo controle VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Atributo de controle ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a888df328062a81637b36dc3fcfbe178d6e49bd4aee01c65b2d2e3524fb321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379921"
---
# <a name="controlshowrollbackcost-control-attribute"></a>Atributo de controle ControlShowRollbackCost

Esse atributo especifica se os arquivos de backup de redução estão incluídos ou não nos custos exibidos pelo [controle VolumeCostList](volumecostlist-control.md).

Se esse bit estiver definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de redução serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).

Se esse bit não estiver definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de redução não serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controles válidos

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Comentários

Esse atributo de controle será ignorado se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou F.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, o custo da redução, os arquivos de backup serão incluídos.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou [**propriedade DISABLEROLLBACK**](-disablerollback.md) = 1, o custo da redução, os arquivos de backup não serão incluídos.

 

 



