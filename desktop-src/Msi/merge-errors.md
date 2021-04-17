---
description: A propriedade de erros somente leitura do objeto de mesclagem retorna uma coleção de objetos de erro que é o conjunto atual de erros.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Propriedade Merge. Errors (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750803"
---
# <a name="mergeerrors-property"></a>Propriedade Merge. Errors

A propriedade de **erros** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção de objetos de [**erro**](error-object.md) que é o conjunto atual de erros.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

A recuperação não é destrutiva. Várias instâncias da coleção de erros podem ser recuperadas chamando esse método repetidamente.

### <a name="c"></a>C++

Consulte a função [**obter \_ erros**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
