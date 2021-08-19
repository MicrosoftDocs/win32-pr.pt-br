---
title: Método StringCollection.getItemInfoByType
description: O método getItemInfoByType recupera o valor correspondente ao índice, nome, idioma e atributo StringCollection especificado.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Método getItemInfoByType Windows Media Player
- Método getItemInfoByType Windows Media Player classe , StringCollection
- Classe StringCollection Windows Media Player método , getItemInfoByType
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
ms.openlocfilehash: 7b9d270ab746618f81f7c2e4135f7a6057f207d2cc89961ebe7c8f47d9fd1abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123026"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>Método StringCollection.getItemInfoByType

O **método getItemInfoByType** recupera o valor correspondente ao índice, nome, idioma e atributo **StringCollection** especificado.

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

*índice* \[ Em\]
</dt> <dd>

**Number** (**long**) especificando o índice baseado em zero do item **StringCollection** do qual obter o atributo.

</dd> <dt>

*name* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o nome do atributo.

</dd> <dt>

*idioma* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o idioma. Se o valor for definido como nulo ou a cadeia de caracteres vazia ("") a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> <dt>

*attributeIndex* \[ Em\]
</dt> <dd>

**Number** (**long**) que contém o índice baseado em zero do valor a ser recuperado do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Number**, **String**, **MetadataPicture** ou **objeto MetadataText,** conforme indicado na tabela a seguir.



| Atributo                   | Valor retornado                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **Number** (**unsigned long**) |
| **\_WM/Synchronizado** | **Objeto MetadataText**        |
| **WM/Picture**              | **Objeto MetadataPicture**     |
| **WM/UserWebURL**           | **Objeto MetadataText**        |
| Todos os outros atributos        | String                         |



 

Para atributos cujo valor subjacente é **booliana,** esse método retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Esse método dá suporte a atributos com vários valores e atributos com valores complexos. O **método getItemInfo** não dá suporte a atributos com valores múltiplos ou complexos.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

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

[**StringCollection.getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**Objeto StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





