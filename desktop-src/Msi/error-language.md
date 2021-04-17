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
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747980"
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
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

