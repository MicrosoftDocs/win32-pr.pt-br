---
title: Método IWMPPlaylist insertItem
description: O método insertItem insere um item de mídia em um local especificado em uma playlist.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- Método insertItem Windows Media Player
- Método insertItem Windows Media Player , interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player , método insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10717c0891443aaa663b748be6a0cb57e04e58b96beb91db6b02b2f6a4b5b621
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464926"
---
# <a name="iwmpplaylistinsertitem-method"></a>Método IWMPPlaylist::insertItem

O **método insertItem** insere um item de mídia em um local especificado em uma playlist.

## <a name="syntax"></a>Sintaxe


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndex* \[ Em\]
</dt> <dd>

Um **System.Int32 que** é o índice baseado em zero no qual o item de mídia será inserido na playlist.

</dd> <dt>

*pIWMPMedia* \[ Em\]
</dt> <dd>

Uma interface **WMPLib.IWMPMedia** que representa o item de mídia a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens de mídia após o item inserido terão seus índices aumentados em um.

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.removeItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





