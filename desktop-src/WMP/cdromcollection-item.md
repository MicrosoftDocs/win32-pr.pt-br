---
title: Método cdromCollection. Item
description: O método item recupera o objeto cdrom no índice fornecido.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método de item Windows Media Player
- método item Windows Media Player, cdromcollection classe
- classe cdromcollection Windows Media Player, método de item
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
ms.openlocfilehash: a5f700a17c29c382e96a5601bd9bbfabf3c4ede1b253d9f271b1d37ab1106ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864076"
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

## <a name="return-value"></a>Valor retornado

Esse método retorna um objeto de **cdrom** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *cdromcollection*. **Item** para imprimir o nome da playlist de cada CD disponível no computador. se a unidade realmente contiver conteúdo de DVD, Windows XP ou posterior será necessário. Um elemento de TextArea HTML foi criado com ID = "playlists". O objeto de **jogador** foi criado com ID = "Player".


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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





