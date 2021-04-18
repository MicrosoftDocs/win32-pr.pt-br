---
title: Propriedade IWMPPlaylist attributeCount
description: A propriedade attributeCount Obtém o número de atributos associados a uma lista de reprodução.
ms.assetid: 0713ec4e-7e06-4ad2-8f7c-17ed5a92d5ee
keywords:
- Propriedade attributeCount Windows Media Player
- Propriedade attributeCount Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, Propriedade attributeCount
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4107eb1ad302415715b573b55d2dee1d7155128d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781149"
---
# <a name="iwmpplaylistattributecount-property"></a>Propriedade IWMPPlaylist:: attributeCount

A propriedade **attributeCount** Obtém o número de atributos associados a uma lista de reprodução.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 attributeCount {get; set;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Valor da propriedade

Um **System. Int32** que é o número de atributos associados à playlist.

## <a name="remarks"></a>Comentários

Como as listas de reprodução podem vir de várias fontes diferentes, elas podem ter vários conjuntos de atributos diferentes. Essa propriedade Obtém o número total de atributos associados a uma lista de reprodução específica para que outros membros da interface **IWMPPlaylist** possam acessá-los.

Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Para obter mais informações sobre atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir ilustra como várias propriedades e métodos das interfaces **IWMPPlaylist** e **IWMPMedia** são usadas preenchendo um controle TreeView com nós para a lista de reprodução atual, atributos de playlist, itens de mídia na lista de reprodução e atributos de item de mídia. O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.


```CSharp
WMPLib.IWMPPlaylist playlist = player.currentPlaylist;
WMPLib.IWMPMedia media;
string name;

// Demonstrates setItemInfo()
playlist.setItemInfo("custom playlist attribute", "changed");
playlist.get_Item(0).setItemInfo("new custom attribute", "5");

// Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
System.Windows.Forms.TreeNode playlistRootNode = new System.Windows.Forms.TreeNode("Playlist Attributes");

for (int i = 0; i < playlist.attributeCount; ++i)
{
    // Add a tree node for each playlist attribute.
    string attribute = playlist.get_attributeName(i);
    playlistRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(attribute));

    // Add a subnode for the item info for that attribute.
    string info = playlist.getItemInfo(attribute);
    playlistRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(info));
}

// Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode);

// Add nodes for each media item and subnodes for each attribute of that item.
System.Windows.Forms.TreeNode mediaRootNode = new System.Windows.Forms.TreeNode("Media Items in the Playlist");
for(int i = 0; i < playlist.count; i++)
{
    // Get the media item
    media = playlist.get_Item(i);

    // Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(media.name));

    // Add a child node for each attribute of the media item
    for(int j = 0; j < media.attributeCount; j++)
    {
        name = media.getAttributeName(j);
        mediaRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(name + ": " + media.getItemInfo(name)));
    }
}

// Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode);
```


```VB

Dim playlist As WMPLib.IWMPPlaylist = player.currentPlaylist
Dim Media As WMPLib.IWMPMedia
Dim name As String

&#39; Demonstrates setItemInfo()
playlist.setItemInfo(&quot;custom playlist attribute&quot;, &quot;changed&quot;)
playlist.Item(0).setItemInfo(&quot;new custom attribute&quot;, &quot;5&quot;)

&#39; Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
Dim playlistRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Playlist Attributes&quot;)

For i As Integer = 0 To (playlist.attributeCount - 1) Step 1

    &#39; Add a tree node for each playlist attribute.
    Dim attribute As String = playlist.attributeName(i)
    playlistRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(attribute))

    &#39; Add a subnode for the item info for that attribute.
    Dim info As String = playlist.getItemInfo(attribute)
    playlistRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(info))

Next i

&#39; Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode)

&#39; Add nodes for each media item and subnodes for each attribute of that item.
Dim mediaRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Media Items in the Playlist&quot;)

For i As Integer = 0 To (playlist.count - 1) Step 1

    &#39; Get the media item
    Media = playlist.Item(i)

    &#39; Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(Media.name))

    &#39; Add a child node for each attribute of the media item
    For j As Integer = 0 To (Media.attributeCount - 1) Step 1

        name = Media.getAttributeName(j)
        mediaRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(name + &quot;: &quot; + Media.getItemInfo(name)))

    Next j

Next i

&#39; Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode)
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





