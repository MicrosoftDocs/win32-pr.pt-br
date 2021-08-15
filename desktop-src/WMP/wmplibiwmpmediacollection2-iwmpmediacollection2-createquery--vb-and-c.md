---
title: Método IWMPMediaCollection2 createQuery
description: O método createQuery retorna uma interface IWMPQuery que representa uma nova consulta.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- Windows Media Player do método createQuery
- método createQuery Windows Media Player, interface IWMPMediaCollection2
- Windows Media Player de interface IWMPMediaCollection2, método createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1644748008e2b222fef0101a96892d480ad4723b9892b94e0e69c387b54e53d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000086"
---
# <a name="iwmpmediacollection2createquery-method"></a>Método IWMPMediaCollection2:: createQuery

O `createQuery` método retorna uma interface **IWMPQuery** que representa uma nova consulta.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib. IWMPQuery** que representa uma nova consulta vazia.

## <a name="remarks"></a>Comentários

A criação de uma nova consulta é a primeira etapa para criar uma consulta composta.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa `createQuery` para obter uma interface **IWMPQuery** que é inicializada como nula. Como essa consulta não tem condições adicionadas a ela, quando ela é usada como um argumento no método **getStringCollectionByQuery** , o método retornará uma coleção de cadeias de caracteres que contém todos os itens de mídia do tipo de mídia especificado. A coleção de cadeia de caracteres é exibida em uma caixa de listagem.


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

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

[**Interface IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





