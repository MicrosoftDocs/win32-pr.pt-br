---
description: A propriedade DatabaseKeys somente leitura do objeto Error retorna uma coleção de cadeias de caracteres que contém as chaves primárias da linha do banco de dados que está causando o erro. Há uma chave por entrada na coleção.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Propriedade Error.DatabaseKeys (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 075fba028dd045c831adb84a7133fd524398fc74037b7e3c31116b76a4c95a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086036"
---
# <a name="errordatabasekeys-property"></a>Propriedade Error.DatabaseKeys

A propriedade **DatabaseKeys** somente leitura do objeto [**Error**](error-object.md) retorna uma coleção de cadeias de caracteres que contém as chaves primárias da linha do banco de dados que está causando o erro. Há uma chave por entrada na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

O cliente é responsável por liberar a coleção de cadeias de caracteres quando ela não é mais necessária.

A coleção será vazia se os valores não se aplicarem ao tipo do erro. Você pode determinar o tipo de erro chamando a [**propriedade Type**](error-type.md) do [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Confira [**obter a função \_ DatabaseKeys.**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

