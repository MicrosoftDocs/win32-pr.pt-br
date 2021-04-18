---
title: Método addcondition IWMPQuery
description: O método addcondition adiciona uma condição à consulta composta usando AND Logic.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- método addcondition do Windows Media Player
- método addcondition Windows Media Player, interface IWMPQuery
- Interface IWMPQuery Windows Media Player, método addcondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764170"
---
# <a name="iwmpqueryaddcondition-method"></a>Método IWMPQuery:: addcondition

O método **addcondition** adiciona uma condição à consulta composta usando **and** Logic.

## <a name="syntax"></a>Sintaxe


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrattribute* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do atributo a ser adicionado à consulta.

</dd> <dt>

*bstrOperator* \[ no\]
</dt> <dd>

Um **System. String** que é o operador. Consulte comentários para obter os valores com suporte.

</dd> <dt>

*bstrvalue* \[ no\]
</dt> <dd>

Um **System. String** que é o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

As condições contidas em uma consulta composta são organizadas em grupos de condição. Várias condições dentro de um grupo de condição são sempre concatenadas usando **and** lógica. Os grupos de condição sempre são concatenados entre si usando **ou** lógica. Para iniciar um novo grupo de condição, chame [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

As consultas compostas usando **IWMPQuery** não diferenciam maiúsculas de minúsculas.

Uma lista de valores para o parâmetro *bstrattribute* pode ser encontrada em [referência de atributo alfabética](alphabetical-attribute-reference.md).

A tabela a seguir lista os valores com suporte para *bstrOperator*.



| String              | Aplica-se a     |
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

O exemplo a seguir cria uma consulta, adiciona duas condições a ela e usa essa consulta para extrair os resultados da consulta como uma coleção de cadeia de caracteres. Os resultados são exibidos em uma caixa de listagem. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo alfabético**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2. createQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getPlaylistByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





