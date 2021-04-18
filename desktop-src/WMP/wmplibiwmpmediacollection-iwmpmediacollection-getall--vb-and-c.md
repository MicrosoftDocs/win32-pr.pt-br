---
title: Método IWMPMediaCollection getAll
description: O método getAll retorna uma interface IWMPPlaylist que corresponde à playlist que contém todos os itens de mídia na biblioteca.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- método getAll Windows Media Player
- método getAll Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750729"
---
# <a name="iwmpmediacollectiongetall-method"></a>Método IWMPMediaCollection:: getAll

O método **getAll** retorna uma interface **IWMPPlaylist** que corresponde à playlist que contém todos os itens de mídia na biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

A interface **WMPLib. IWMPPlaylist** da lista de reprodução que contém todos os itens de mídia solicitados.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getAll** depende de quais dessas duas maneiras você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getAll** retornará todos os itens de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getAll** retornará apenas os itens de áudio na biblioteca.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **getAll** para reproduzir itens de mídia aleatoriamente da coleção de mídias. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
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

 

 





