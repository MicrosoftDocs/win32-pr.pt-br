---
title: Método getAll IWMPPlaylistCollection
description: O método getAll retorna uma interface IWMPPlaylistArray que fornece acesso a todas as playlists na biblioteca.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- Método getAll Windows Media Player
- interface getAll Windows Media Player , IWMPPlaylistCollection
- Interface IWMPPlaylistCollection Windows Media Player método , getAll
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ff50c2983d911e7aa3951e34f908d9982b623912539aa4e162c9cccb2f5256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568443"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>Método IWMPPlaylistCollection::getAll

O **método getAll** retorna uma interface **IWMPPlaylistArray** que fornece acesso a todas as playlists na biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Uma interface **WMPLib.IWMPPlaylistArray** para a matriz recuperada de playlists.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





