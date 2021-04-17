---
description: A propriedade Format do objeto ConfigurableItem retorna o valor da coluna Format da Tabela ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Propriedade ConfigurableItem. Format (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747778"
---
# <a name="configurableitemformat-property"></a>Propriedade ConfigurableItem. Format

A propriedade **Format** do objeto [**ConfigurableItem**](configurableitem-object.md) retorna o valor da coluna Format da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Esta propriedade só pode ter os valores a seguir.



| Constante                        | Valor |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

Consulte [**obter \_**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) função de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




