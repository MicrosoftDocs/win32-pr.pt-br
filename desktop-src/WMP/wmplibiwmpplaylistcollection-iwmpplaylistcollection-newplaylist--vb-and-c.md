---
title: Método IWMPPlaylistCollection newPlaylist
description: O método newPlaylist retorna uma interface IWMPPlaylist para uma lista de reprodução nova e vazia na biblioteca.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811699"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>Método IWMPPlaylistCollection:: newPlaylist

O método **newPlaylist** retorna uma interface **IWMPPlaylist** para uma lista de reprodução nova e vazia na biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Um **System. String** que é o nome da nova lista de reprodução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para a nova lista de reprodução.

## <a name="remarks"></a>Comentários

Esse método cria uma lista de reprodução vazia na biblioteca. Para preencher a lista de reprodução com itens de mídia, use **IWMPPlaylist. appendItem** ou **IWMPPlaylist. insertItem**.

Várias listas de reprodução com o mesmo nome são permitidas na biblioteca. Para evitar a criação de um nome de playlist duplicado com esse método, use o método **getByName** e **IWMPPlaylistArray. Count** para descobrir se uma lista de reprodução com um nome específico já existe.

Espaços à esquerda e à direita não são permitidos em nomes de playlist e são removidos automaticamente do valor especificado para o parâmetro *bstrname* .

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir cria uma nova lista de reprodução vazia chamada "3list", adiciona-a à coleção de playlist e retorna uma interface a ela. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Count (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





