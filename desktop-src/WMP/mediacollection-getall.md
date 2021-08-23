---
title: Método mediacollection. getAll
description: O método getAll recupera uma lista de reprodução que contém todos os itens de mídia na biblioteca.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- Windows Media Player do método getAll
- método getAll Windows Media Player, classe mediacollection
- classe mediacollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3bba961f9400470c16e3d773a5765d389ce05bc23c2e948f0b94c7ad22229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135059"
---
# <a name="mediacollectiongetall-method"></a>Método mediacollection. getAll

O método **getAll** recupera uma lista de reprodução que contém todos os itens de mídia na biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna um objeto **playlist** .

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mediacollection*. **getAll** para reproduzir itens de mídia aleatoriamente da coleção de mídias. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto playlist**](playlist-object.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





