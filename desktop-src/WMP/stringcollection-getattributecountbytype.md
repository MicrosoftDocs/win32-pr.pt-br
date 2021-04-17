---
title: Método StringCollection. getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao índice do item StringCollection especificado, ao nome do atributo e ao idioma.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811949"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>Método StringCollection. getAttributeCountByType

O método **getAttributeCountByType** recupera o número de atributos associados ao índice do item **StringCollection** especificado, ao nome do atributo e ao idioma.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) especificando o índice de base zero do item **StringCollection** do qual obter o atributo.

</dd> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo.

</dd> <dt>

*idioma* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o idioma. Se o valor for definido como nulo ou a cadeia de caracteres vazia (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Esse método é usado para determinar o número de atributos correspondentes a um determinado nome de atributo para um determinado item **StringCollection** . Os números de índice podem então ser passados para o quarto parâmetro do método **StringCollection. getItemInfoByType** .

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





