---
title: Método IWMPPlaylist appendItem
description: O método appendItem adiciona um item de mídia ao final de uma lista de reprodução.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- Windows Media Player do método appendItem
- método appendItem Windows Media Player, interface IWMPPlaylist
- Windows Media Player de interface IWMPPlaylist, método appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de67c7bbd3448e4b4fcdb562b2b10ace68ed7a2c92020650c79fdd90b05366b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098696"
---
# <a name="iwmpplaylistappenditem-method"></a>Método IWMPPlaylist:: appendItem

O método **appendItem** adiciona um item de mídia ao final de uma lista de reprodução.

## <a name="syntax"></a>Sintaxe


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIWMPMedia* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPMedia** que representa o item de mídia a ser anexado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **appendItem** para adicionar o item de mídia atual à lista de reprodução denominada "trêslist". O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





