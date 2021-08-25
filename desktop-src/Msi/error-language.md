---
description: A propriedade de linguagem somente leitura do objeto de erro retorna o LANGid do erro atual.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propriedade Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082886"
---
# <a name="errorlanguage-property"></a>Propriedade Error. Language

A propriedade de **linguagem** somente leitura do objeto de [**erro**](error-object.md) retorna o **LangID** do erro atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

O valor da propriedade **Language** é-1, a menos que o erro seja do tipo MsmErrorLanguageUnsupported ou msmErrorLanguageFailed. Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .

### <a name="c"></a>C++

Consulte [**a \_ função obter linguagem (objeto de erro)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

