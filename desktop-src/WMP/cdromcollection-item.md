---
title: Método cdromCollection. Item
description: O método item recupera o objeto cdrom no índice fornecido.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe cdromCollection
- Classe cdromCollection Windows Media Player, método de item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796438"
---
# <a name="cdromcollectionitem-method"></a>Método cdromCollection. Item

O método **Item** recupera o objeto **cdrom** no índice fornecido.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

**Número** (**longo**) que contém o índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto de **cdrom** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *cdromCollection*. **Item** para imprimir o nome da playlist de cada CD disponível no computador. Se a unidade realmente contiver conteúdo de DVD, o Windows XP ou posterior será necessário. Um elemento de TextArea HTML foi criado com ID = "playlists". O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cdrom. driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Objeto cdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection. contagem**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





