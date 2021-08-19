---
title: Playlist. attributeCount
description: A propriedade attributeCount recupera o número de atributos associados à playlist.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Windows Media Player de playlist. attributeCount
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63616096dbfc3989a93d3dc8010dd0ed1f256ccd9e9bf2cc7b3c825c88a63d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054294"
---
# <a name="playlistattributecount"></a>Playlist. attributeCount

A propriedade **attributeCount** recupera o número de atributos associados à playlist.

## <a name="syntax"></a>Syntax

*Player*. *currentPlaylist*. **attributeCount**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Como as listas de reprodução podem vir de várias fontes diferentes, elas podem ter vários conjuntos diferentes de propriedades. Esse método recupera o número total de propriedades disponíveis para que os outros métodos do objeto **playlist** possam acessá-las.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

para obter informações sobre os atributos com suporte pelo Windows Media Player, consulte a [referência de atributo](attribute-reference.md)Windows Media Player.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript ilustra como várias propriedades e métodos da **Playlist** e dos objetos de **mídia** são usados.


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. attributeName**](playlist-attributename.md)
</dt> <dt>

[**Playlist. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





