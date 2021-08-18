---
description: A propriedade Moduletable somente leitura retorna o nome da tabela no módulo que causou o erro.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Erro. Propriedade Moduletable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 47cd9bab5c12230a048da04e60169e1ad21195df2304642f6b656983539f3b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947052"
---
# <a name="errormoduletable-property"></a>Erro. Propriedade Moduletable

A propriedade **moduletable** somente leitura retorna o nome da tabela no módulo que causou o erro.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

A coleção estará vazia se os valores não se aplicarem ao tipo do erro. Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**obter a função \_ moduletable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

