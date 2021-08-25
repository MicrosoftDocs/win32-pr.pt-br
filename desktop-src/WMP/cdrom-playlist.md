---
title: Cdrom.playlist
description: A propriedade playlist recupera um objeto Playlist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título de nível raiz para DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom.playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29419b68c50718165e49c0fbe9e75487e9154c19243453981ab352f03e8209a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864176"
---
# <a name="cdromplaylist"></a>Cdrom.playlist

A **propriedade playlist** recupera um objeto **Playlist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título de nível raiz para DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um objeto playlist **somente** leitura.

## <a name="remarks"></a>Comentários

Normalmente, DVDs são organizados em títulos. Cada título contém um ou mais capítulos. Cada DVD é escrito de forma diferente, portanto, a maneira como títulos e capítulos são usados é de acordo com o autor do conteúdo.

Para DVD, esse método recupera uma playlist que contém como o primeiro item um **objeto Media** que representa a mídia de DVD. Reproduzir o item resulta na reprodução do DVD desde o início se for a primeira reprodução depois de inserir um novo DVD ou retomar a reprodução se o DVD for o mesmo que o último DVD exibido. Definir esse item como o atual durante a reprodução resulta na reprodução do DVD desde o início.

Itens adicionais (**objetos de** mídia) na playlist são títulos de DVD representados por playlists aninhadas. Quando você especifica *Controles*. **currentItem para** ser igual a um desses itens de playlist aninhados, Windows Media Player define automaticamente a playlist aninhada como *Player*. **currentPlaylist após** o início da reprodução do capítulo. Em seguida, você pode usar as propriedades, os métodos e os eventos do objeto **currentPlaylist** para trabalhar com capítulos de DVD, que também são itens de playlist.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa *Cdrom*. **playlist** para preencher um elemento de texto HTML, chamado myText, com os títulos do CD de áudio atualmente na primeira unidade de CD. Use *CdromCollection*. **contagem** para determinar o número de unidades de CD disponíveis. O **objeto** Player foi criado com ID = "Player".


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Versão<br/>                  | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Cdrom**](cdrom-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





