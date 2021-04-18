---
title: Método IWMPPlaylistCollection getByName
description: O método getByName retorna uma interface IWMPPlaylistArray que fornece acesso a listas de reprodução com o nome especificado, se existir.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771619"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a>Método IWMPPlaylistCollection:: getByName

O método **getByName** retorna uma interface **IWMPPlaylistArray** que fornece acesso a listas de reprodução com o nome especificado, se existir.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Um **System. String** que é o nome da playlist.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylistArray** para a matriz de listas de reprodução recuperada.

## <a name="remarks"></a>Comentários

Use **IWMPPlaylistArray. Count** para determinar se existe uma lista de reprodução. Se **Count** for zero, a matriz estará vazia.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **getByName** para verificar a coleção de playlist de uma lista de reprodução chamada "favoritos--4 e 5 estrelas classificados". Se existir uma lista de reprodução com esse nome, **getByName** a definirá como a playlist atual. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Count (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





