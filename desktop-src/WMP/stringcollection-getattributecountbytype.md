---
title: Método StringCollection.getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao índice de item StringCollection, ao nome do atributo e ao idioma especificados.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Método getAttributeCountByType Windows Media Player
- Método getAttributeCountByType Windows Media Player classe , StringCollection
- Classe StringCollection Windows Media Player método , getAttributeCountByType
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
ms.openlocfilehash: 2e10f88a3b8e4847588ff8f7f924333c6649e59c362b3296b54ef8b83368b7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832423"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>Método StringCollection.getAttributeCountByType

O **método getAttributeCountByType** recupera o número de atributos associados ao índice de item **StringCollection,** ao nome do atributo e ao idioma especificados.

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

*índice* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice baseado em zero do item **StringCollection** do qual obter o atributo.

</dd> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que contém o nome do atributo.

</dd> <dt>

*idioma* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o idioma. Se o valor for definido como nulo ou a cadeia de caracteres vazia (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **Número** (**long**).

## <a name="remarks"></a>Comentários

Esse método é usado para determinar o número de atributos correspondentes a um nome de atributo específico para um item **StringCollection** específico. Os números de índice podem ser passados para o quarto parâmetro do **método StringCollection.getItemInfoByType.**

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





