---
description: A propriedade Format do objeto ConfigurableItem retorna o valor da coluna Formato da tabela ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Propriedade ConfigurableItem.Format (Mergemod.h)
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
ms.openlocfilehash: ee8770029c8465d1e1a60349010847ff38fdac928bb61cd02b0e5a2b034538c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143993"
---
# <a name="configurableitemformat-property"></a>Propriedade ConfigurableItem.Format

A **propriedade Format** do objeto [**ConfigurableItem**](configurableitem-object.md) retorna o valor da coluna Formato da tabela [ModuleConfiguration](moduleconfiguration-table.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Essa propriedade só pode ter os valores a seguir.



| Constante                        | Valor |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

Consulte [**obter \_ a função**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) Format.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




