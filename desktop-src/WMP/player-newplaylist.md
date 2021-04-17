---
title: Método Player. newPlaylist
description: O método newPlaylist cria um novo objeto de lista de reprodução.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- método newPlaylist Windows Media Player
- método newPlaylist Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763052"
---
# <a name="playernewplaylist-method"></a>Método Player. newPlaylist

O método **newPlaylist** cria um novo objeto de **lista de reprodução** .

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém o nome da nova lista de reprodução.

</dd> <dt>

*URL* \[ do no\]
</dt> <dd>

**Cadeia de caracteres** que contém a URL da lista de reprodução do metarquivo do Windows Media com a qual criar o objeto de **playlist** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Se o parâmetro de *URL* for definido como nulo ou "" (cadeia de caracteres vazia), um objeto de **playlist** vazio será criado. Se o parâmetro *Name* for definido como "", o nome no metarquivo será usado.

A nova lista de reprodução criada com esse método não é adicionada à biblioteca. Para adicionar uma nova lista de reprodução à biblioteca, use *playlistcollection*. **importPlaylist** ou *playlistcollection*. **newPlaylist**. Os espaços à esquerda ou à direita no nome da playlist são removidos automaticamente quando adicionados à biblioteca.

Como a biblioteca permite várias listas de reprodução com o mesmo nome, talvez você queira verificar a presença de uma lista de reprodução com um nome específico antes de adicionar uma nova.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Playlistcollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Playlistcollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Metaarquivos do Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 





