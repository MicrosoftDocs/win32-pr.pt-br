---
title: Método IWMPPlaylistCollection importPlaylist
description: O método importPlaylist adiciona uma lista de reprodução estática à biblioteca. | Método IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Windows Media Player do método importPlaylist
- método importPlaylist Windows Media Player, interface IWMPPlaylistCollection
- Windows Media Player de interface IWMPPlaylistCollection, método importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee4c231a045b39454908753dc197c95e26d85c711968f07ab27dbd859c29c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122526"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>Método IWMPPlaylistCollection:: importPlaylist

O método **importPlaylist** adiciona uma lista de reprodução estática à biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pItem* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução que esse método adicionará.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma interface **WMPLib. IWMPPlaylist** para a lista de reprodução adicionada.

## <a name="remarks"></a>Comentários

As listas de reprodução que não contêm nenhum item de mídia não podem ser adicionadas à biblioteca usando esse método. Para criar uma lista de reprodução vazia na biblioteca, use o método **newPlaylist** . Em seguida, você pode preencher a lista de reprodução resultante com itens de mídia usando **IWMPPlaylist. appendItem** ou **IWMPPlaylist. insertItem**.

Se você passar esse método para uma lista de reprodução automática, a consulta será executada uma vez e o resultado será adicionado à biblioteca como uma lista de reprodução estática. Para adicionar uma lista de reprodução automática à biblioteca e preservar seu comportamento automático, use **IWMPMediaCollection. Add**. Para obter mais informações, consulte [playlists estáticas e automáticas](static-and-auto-playlists.md).

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPMediaCollection. Add (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





