---
title: Método Query. addcondition
description: O método addcondition adiciona uma condição ao objeto de consulta usando a lógica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- método addcondition do Windows Media Player
- método addcondition Windows Media Player, classe de consulta
- Classe de consulta Windows Media Player, método addcondition
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793271"
---
# <a name="queryaddcondition-method"></a>Método Query. addcondition

O método **addcondition** adiciona uma condição ao objeto de **consulta** usando a lógica and.

## <a name="syntax"></a>Sintaxe


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributo* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome do atributo.

</dd> <dt>

*operador* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém o operador. Consulte comentários para obter os valores com suporte.

</dd> <dt>

*valor* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Consultas compostas usando a **consulta** não diferenciam maiúsculas de minúsculas.

Uma lista de valores para o parâmetro de *atributo* pode ser encontrada na seção [referência de atributo alfabética](alphabetical-attribute-reference.md) .

As condições contidas em um objeto de **consulta** são organizadas em grupos de condição. Várias condições dentro de um grupo de condições sempre são concatenadas usando AND Logic. Os grupos de condição sempre são concatenados entre si usando ou lógica. Para iniciar um novo grupo de condição, chame **Query. beginNextGroup**.

A tabela a seguir lista os valores com suporte para o *operador*.



| Operador            | Aplica-se a     |
|---------------------|----------------|
| BeginsWith          | Cadeias de caracteres        |
| Contém            | Cadeias de caracteres        |
| É igual a              | Todos os tipos      |
| GreaterThan         | Números, datas |
| GreaterThanOrEquals | Números, datas |
| LessThan            | Números, datas |
| LessThanOrEquals    | Números, datas |
| NotBeginsWith       | Cadeias de caracteres        |
| NotContains         | Cadeias de caracteres        |
| NotEquals           | Todos os tipos      |



 

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa **Query. addcondition** e **Query. beginNextGroup** para executar uma consulta de exemplo.


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediacollection. createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Mediacollection. getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objeto de consulta**](query-object.md)
</dt> <dt>

[**Query. beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





