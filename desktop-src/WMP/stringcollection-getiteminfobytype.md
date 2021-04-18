---
title: Método StringCollection. getItemInfoByType
description: O método getItemInfoByType recupera o valor correspondente ao índice, nome, idioma e índice da StringCollection especificados.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791275"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>Método StringCollection. getItemInfoByType

O método **getItemInfoByType** recupera o valor correspondente ao índice, nome, idioma e índice da **StringCollection** especificados.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
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

**Cadeia de caracteres** que contém o idioma. Se o valor for definido como NULL ou a cadeia de caracteres vazia (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> <dt>

*attributeIndex* \[ no\]
</dt> <dd>

**Número** (**longo**) que contém o índice de base zero do valor a ser recuperado do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **número**, uma **cadeia de caracteres**, um objeto **MetadataPicture** ou um objeto **MetadataText** , conforme indicado na tabela a seguir.



| Atributo                   | Retornar valor                   |
|-----------------------------|--------------------------------|
| **Sincronizarstate**               | **Número** (**longo sem sinal**) |
| **WM/letras de música \_ sincronizadas** | Objeto **MetadataText**        |
| **WM/imagem**              | Objeto **MetadataPicture**     |
| **WM/UserWebURL**           | Objeto **MetadataText**        |
| Todos os outros atributos        | String                         |



 

Para atributos cujo valor subjacente é **booliano**, esse método retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O método **getItemInfo** não oferece suporte a atributos com valores múltiplos ou complexos.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Objeto MetadataText**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





