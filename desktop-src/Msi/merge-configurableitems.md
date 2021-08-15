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
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013034"
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
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




