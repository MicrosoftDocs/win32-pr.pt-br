---
title: Método IWMPMediaCollection getByAttribute
description: O método getByAttribute retorna uma interface IWMPPlaylist que corresponde ao atributo especificado com o valor especificado.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- método getByAttribute Windows Media Player
- método getByAttribute Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758904"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>Método IWMPMediaCollection:: getByAttribute

O método **getByAttribute** retorna uma interface **IWMPPlaylist** que corresponde ao atributo especificado com o valor especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrattribute* \[ no\]
</dt> <dd>

O **System. String** que é o atributo especificado.

</dd> <dt>

*bstrvalue* \[ no\]
</dt> <dd>

O **System. String** que é o valor especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.

## <a name="remarks"></a>Comentários

Esse método pode ser usado para criar uma consulta genérica para itens de mídia que correspondem a um valor para um atributo na biblioteca. Isso é útil no caso de atributos definidos pelo usuário. Se o atributo não existir, será resultado um erro.

Você pode usar esse método para recuperar todos os itens de mídia de um tipo específico. Use o nome de atributo **MediaType** e um dos valores a seguir.



| Valor    | Descrição                                               |
|----------|-----------------------------------------------------------|
| áudio    | Música e outros itens somente de áudio                          |
| outros    | Outros itens, como um arquivo. ASF ou a URL de um fluxo. |
| foto    | Itens de foto. Requer o Windows Media Player 10.            |
| playlist | Listas de reprodução representadas como itens de mídia.                     |
| radio    | Itens da estação de rádio. Não usado pelo Windows Media Player 10. |
| video    | Itens de vídeo.                                              |



 

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).

Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getByAttribute** depende de quais dessas duas maneiras você usa. Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getByAttribute** retornará todos os itens de mídia na biblioteca. No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getByAttribute** retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **getByAttribute** para reproduzir todo o conteúdo da biblioteca pelo artista chamado Triode 48. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
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
</dt> <dt>

[**IWMPPlaylistCollection. getAll (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





