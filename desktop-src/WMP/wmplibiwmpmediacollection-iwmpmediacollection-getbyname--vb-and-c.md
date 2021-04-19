---
title: Método IWMPMediaCollection getByName
description: O método getByName retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia com o nome especificado.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755025"
---
# <a name="iwmpmediacollectiongetbyname-method"></a>Método IWMPMediaCollection:: getByName

O `getByName` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia com o nome especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

O **System. String** que é o nome especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Há duas maneiras de se recuperar uma interface **IWMPMediaCollection** , e o comportamento do `getByName` método depende de quais dessas duas maneiras você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o `getByName` método retornará todos os itens de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o `getByName` método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa `getByName` para recuperar três itens da biblioteca. Cada item é acrescentado à playlist atual. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





