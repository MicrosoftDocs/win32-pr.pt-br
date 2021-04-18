---
description: A propriedade ModuleKeys somente leitura do objeto de erro retorna um ponteiro para uma coleção de cadeias de caracteres que contém as chaves primárias da linha no módulo que está causando o erro, uma chave por entrada na coleção.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Propriedade Error. ModuleKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752044"
---
# <a name="errormodulekeys-property"></a>Propriedade Error. ModuleKeys

A propriedade **ModuleKeys** somente leitura do objeto de [**erro**](error-object.md) retorna um ponteiro para uma coleção de cadeias de caracteres que contém as chaves primárias da linha no módulo que está causando o erro, uma chave por entrada na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

O cliente é responsável por liberar a coleção de cadeias de caracteres quando ela não é mais necessária.

A coleção estará vazia se os valores não se aplicarem ao tipo do erro. Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**obter \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) a função ModuleKeys.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

