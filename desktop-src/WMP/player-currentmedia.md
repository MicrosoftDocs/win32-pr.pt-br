---
title: Player. currentMedia
description: A propriedade currentMedia especifica ou recupera o objeto de mídia atual.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Windows Media Player Player. currentMedia
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054394"
---
# <a name="playercurrentmedia"></a>Player. currentMedia

A propriedade **currentMedia** especifica ou recupera o objeto de mídia atual.

## <a name="syntax"></a>Syntax

*Player* . **currentMedia**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto de mídia de leitura/gravação.

## <a name="remarks"></a>Comentários

se o *Configurações*. a propriedade **AutoStart** é true, a reprodução é iniciada automaticamente sempre que você definir **currentMedia**.

Essa propriedade usa um objeto de mídia, que pode ser adquirido usando a *lista de reprodução*. **Item**. Para carregar um item de **mídia** usando um nome de arquivo, defina a propriedade URL ou use **newMedia**.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript recupera o primeiro item de mídia na biblioteca. Em seguida, ele usa **currentMedia** para tornar o item de mídia recuperado o item de mídia atual e, em seguida, exibir o nome do item de mídia atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Lista de reprodução. Item**](playlist-item.md)
</dt> <dt>

[**Configurações. autostart**](settings-autostart.md)
</dt> </dl>

 

 





