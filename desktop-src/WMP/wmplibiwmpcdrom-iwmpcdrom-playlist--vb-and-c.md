---
title: Propriedade de playlist IWMPCdrom
description: A propriedade playlist Obtém uma interface IWMPPlaylist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz de um DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Propriedade playlist Windows Media Player
- Propriedade playlist Windows Media Player, interface IWMPCdrom
- Interface IWMPCdrom Windows Media Player, Propriedade playlist
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
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765032"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPCdrom: Propriedade laylist de:P

A propriedade **playlist** Obtém uma interface **IWMPPlaylist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz de um DVD.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valor da propriedade

Uma interface **WMPLib. IWMPPlaylist** .

## <a name="remarks"></a>Comentários

Normalmente, o conteúdo baseado em DVD é organizado em títulos. Cada título contém um ou mais capítulos. Cada DVD é criado de forma diferente, portanto, como os títulos e capítulos são usados, cabe ao autor do conteúdo.

Para um DVD, essa propriedade Obtém uma lista de reprodução que contém como o primeiro item uma interface **IWMPMedia** chamada "DVD". Essa interface representa a mídia de DVD. A reprodução dos resultados do item no DVD será reproduzida desde o início se for a primeira reprodução após a inserção de um novo DVD ou a retomada da reprodução se o DVD for o mesmo que o último DVD exibido. Definir esse item como o item atual durante os resultados da reprodução no DVD é reproduzido desde o início.

Itens adicionais (representados por interfaces **IWMPMedia** ) na playlist são títulos de DVD que são representados por listas de reprodução aninhadas. Quando você define **IWMPControls. currentItem** como igual a um desses itens aninhados da lista de reprodução, o Windows Media Player define automaticamente a lista de reprodução aninhada como a lista de reprodução atual após a execução do capítulo começar. Você pode usar as propriedades de interface **IWMPPlaylist** , métodos e eventos associados para trabalhar com capítulos de DVD, que também são itens de playlist.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **playlist** para preencher uma caixa de texto de várias linhas, chamada mytext, com a lista Track do CD de áudio atualmente na primeira unidade de CD. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


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
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





