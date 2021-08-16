---
title: Método Query.addCondition
description: O método addCondition adiciona uma condição ao objeto Consulta usando a lógica AND.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Método addCondition Windows Media Player
- método addCondition Windows Media Player classe , Query
- Classe de consulta Windows Media Player , método addCondition
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
ms.openlocfilehash: 53a3eed0a7923b93861eabc30d115a7726046d0595b7c57625d9a9afaf9c7523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746585"
---
# <a name="queryaddcondition-method"></a>Método Query.addCondition

O **método addCondition** adiciona uma condição ao **objeto Consulta** usando a lógica AND.

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

*atributo* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o nome do atributo.

</dd> <dt>

*operador* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o operador . Consulte Comentários para ver os valores com suporte.

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Consultas compostas que **usam Consulta não** são sensíveis a minúsculas.

Uma lista de valores para o *parâmetro de* atributo pode ser encontrada na seção Referência de [Atributo Alfabético.](alphabetical-attribute-reference.md)

As condições contidas em **um objeto Query** são organizadas em grupos de condição. Várias condições em um grupo de condições são sempre concatenadas usando a lógica AND. Os grupos de condição são sempre concatenados entre si usando a lógica OR. Para iniciar um novo grupo de condições, **chame Query.beginNextGroup.**

A tabela a seguir lista os valores com suporte para o *operador*.



| Operador            | Aplica-se a     |
|---------------------|----------------|
| BeginsWith          | Cadeias de caracteres        |
| Contém            | Cadeias de caracteres        |
| Igual a              | Todos os tipos      |
| GreaterThan         | Números, Datas |
| GreaterThanOrEquals | Números, Datas |
| LessThan            | Números, Datas |
| LessThanOrEquals    | Números, Datas |
| NotBeginsWith       | Cadeias de caracteres        |
| NotContains         | Cadeias de caracteres        |
| NotEquals           | Todos os tipos      |



 

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa **Query.addCondition** e **Query.beginNextGroup** para executar uma consulta de exemplo.


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

[**MediaCollection.createQuery**](mediacollection-createquery.md)
</dt> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**MediaCollection.getStringCollectionByQuery**](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[**Objeto Query**](query-object.md)
</dt> <dt>

[**Query.beginNextGroup**](query-beginnextgroup.md)
</dt> </dl>

 

 





