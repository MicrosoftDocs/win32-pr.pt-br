---
title: Propriedade playlist IWMPCdrom
description: A propriedade Playlist obtém uma interface IWMPPlaylist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título de nível raiz para um DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propriedades da playlist Windows Media Player
- Propriedade playlist Windows Media Player , interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player , propriedade Playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ff17e3716f01308957b3f5f247759fb3f18f639f7b279a8f00d7f6f9e2189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116597"
---
# <a name="iwmpcdromplaylist-property"></a>Propriedade IWMPCdrom::P laylist

A **propriedade Playlist** obtém uma interface **IWMPPlaylist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título de nível raiz para um DVD.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valor da propriedade

Uma interface **WMPLib.IWMPPlaylist.**

## <a name="remarks"></a>Comentários

Normalmente, o conteúdo baseado em DVD é organizado em títulos. Cada título contém um ou mais capítulos. Cada DVD é escrito de forma diferente, portanto, a maneira como títulos e capítulos são usados é de acordo com o autor do conteúdo.

Para um DVD, essa propriedade obtém uma playlist que contém como o primeiro item uma interface **IWMPMedia** chamada "DVD". Essa interface representa a mídia de DVD. Reproduzir o item resulta na reprodução do DVD desde o início se for a primeira reprodução depois de inserir um novo DVD ou retomar a reprodução se o DVD for o mesmo que o último DVD exibido. Definir esse item como o item atual durante a reprodução resulta na reprodução do DVD desde o início.

Itens adicionais (representados por interfaces **IWMPMedia)** na playlist são títulos de DVD representados por playlists aninhadas. Quando você define **IWMPControls.currentItem** como igual a um desses itens de playlist aninhados, Windows Media Player define automaticamente a playlist aninhada como a playlist atual após o início da reprodução do capítulo. Em seguida, você pode usar as propriedades da interface **IWMPPlaylist,** os métodos e os eventos associados para trabalhar com capítulos de DVD, que também são itens de playlist.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **Playlist** para preencher uma caixa de texto de várias linhas, chamada myText, com a lista de faixas do CD de áudio atualmente na primeira unidade de CD. O **objeto AxWMPLib.AxWindowsMediaPlayer** é representado pela variável chamada player.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





