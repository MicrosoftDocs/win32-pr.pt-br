---
title: Método IWMPMediaCollection Add
description: O método add adiciona um novo item de mídia ou lista de reprodução à biblioteca. | Método IWMPMediaCollection Add
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Adicionar método Windows Media Player
- adicionar método Windows Media Player, interface IWMPMediaCollection
- Windows Media Player de interface IWMPMediaCollection, método add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 778850da4094d8ac745018b115248de9008d15339b7ffee75de177cf957d3fc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861147"
---
# <a name="iwmpmediacollectionadd-method"></a>Método IWMPMediaCollection:: Add

O método **Add** adiciona um novo item de mídia ou lista de reprodução à biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrURL* \[ no\]
</dt> <dd>

Um **System. String** que é a URL que especifica o local do item de mídia ou da lista de reprodução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A interface **WMPLib. IWMPMedia** para o item adicionado ou a lista de reprodução.

## <a name="remarks"></a>Comentários

Esse método carrega um item de mídia existente ou uma lista de reprodução na biblioteca, dado um caminho. Esse método não move nem altera o arquivo. Esse método falhará se um caminho local inválido for fornecido, mas os próprios itens de mídia não serão verificados quanto à validade antes de serem adicionados à biblioteca.

Esse método aceita arquivos de lista de reprodução estáticos e automáticos. O método **IWMPPlaylistCollection. importPlaylist** também pode ser usado para adicionar uma lista de reprodução estática à biblioteca.

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

o exemplo a seguir adiciona três objetos de mídia à coleção de mídia Windows Media Player. O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
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

[**IWMPMediaCollection. Remove (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





