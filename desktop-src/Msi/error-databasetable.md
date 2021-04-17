---
description: A propriedade somente leitura databasetable do objeto de erro retorna o nome da tabela no banco de dados que causou o erro.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Error. Propriedade databasetable (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752655"
---
# <a name="errordatabasetable-property"></a>Erro. Propriedade databasetable

A propriedade somente leitura **databasetable** do objeto de [**erro**](error-object.md) retorna o nome da tabela no banco de dados que causou o erro.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

A coleção estará vazia se os valores não se aplicarem ao tipo do erro. Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**obter a função \_ databasetable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

