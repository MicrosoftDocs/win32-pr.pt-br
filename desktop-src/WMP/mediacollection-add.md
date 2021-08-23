---
title: Método MediaCollection.add
description: O método add adiciona um novo item de mídia ou uma playlist à biblioteca. | Método MediaCollection.add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- adicionar método Windows Media Player
- classe add method Windows Media Player , MediaCollection
- Classe MediaCollection Windows Media Player , adicionar método
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647906"
---
# <a name="mediacollectionadd-method"></a>Método MediaCollection.add

O **método add** adiciona um novo item de mídia ou uma playlist à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*caminho* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que contém o caminho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **objeto Media.**

## <a name="remarks"></a>Comentários

Esse método carrega um item de mídia ou uma playlist existente na biblioteca, dado um caminho para um arquivo. Esse método não move nem altera o arquivo. Esse método falhará se for dado um caminho local inválido, mas os arquivos de mídia digital não serão verificados quanto à validade antes que sejam adicionados à biblioteca.

Esse método aceita arquivos de playlist estáticos e automáticos. O *PlaylistCollection.* **O método importPlaylist** também pode ser usado para adicionar uma playlist estática à biblioteca.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo de JScript Microsoft a seguir adiciona três objetos de mídia à Windows Media Player de mídia. O **objeto** Player foi criado com ID="Player".


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerenciando playlists**](managing-playlists.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.remove**](mediacollection-remove.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





