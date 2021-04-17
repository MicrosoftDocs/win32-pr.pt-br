---
description: A propriedade ConfigurableItems somente leitura do objeto de mesclagem retorna uma coleção ConfigurableItem objetos, cada um representando uma única linha da Tabela ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.ConfigPropriedade urableItems (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759383"
---
# <a name="mergeconfigurableitems-property"></a>Merge.ConfigPropriedade urableItems

A propriedade **ConfigurableItems** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção [**ConfigurableItem**](configurableitem-object.md) objetos, cada um representando uma única linha da [Tabela ModuleConfiguration](moduleconfiguration-table.md). Semanticamente, cada interface no enumerador representa um item que pode ser configurado pelo consumidor do módulo. A coleção é uma coleção somente leitura e implementa as interfaces de coleção somente leitura padrão de item (), Count () e \_ NewEnum (). O enumerador **IEnumMsmConfigItems** implementa Next (), ignore (), Reset () e clone () com a semântica padrão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valor da propriedade

## <a name="c"></a>C++

Consulte [**obter \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) a função ConfigurableItems.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




