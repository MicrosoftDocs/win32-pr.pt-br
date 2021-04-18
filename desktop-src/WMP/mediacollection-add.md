---
title: Método mediacollection. Add
description: O método add adiciona um novo item de mídia ou lista de reprodução à biblioteca. | Método mediacollection. Add
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Adicionar método Windows Media Player
- Adicionar método Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, Adicionar método
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
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788152"
---
# <a name="mediacollectionadd-method"></a>Método mediacollection. Add

O método **Add** adiciona um novo item de mídia ou lista de reprodução à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*caminho* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o caminho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto de **mídia** .

## <a name="remarks"></a>Comentários

Esse método carrega um item de mídia existente ou uma lista de reprodução na biblioteca, dado um caminho para um arquivo. Esse método não move nem altera o arquivo. Esse método falhará se um caminho local inválido for fornecido, mas os arquivos de mídia digital não serão verificados quanto à validade antes de serem adicionados à biblioteca.

Esse método aceita arquivos de lista de reprodução estáticos e automáticos. A *playlistcollection*. o método **importPlaylist** também pode ser usado para adicionar uma lista de reprodução estática à biblioteca.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo do Microsoft JScript a seguir adiciona três objetos de mídia à coleção de mídia do Windows Media Player. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. Remove**](mediacollection-remove.md)
</dt> <dt>

[**Playlistcollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





