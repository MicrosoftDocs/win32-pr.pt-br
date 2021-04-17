---
title: Método IWMPPlaylist insertItem
description: O método insertItem insere um item de mídia em um local especificado em uma lista de reprodução.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- método insertItem Windows Media Player
- método insertItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método insertItem
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
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797951"
---
# <a name="iwmpplaylistinsertitem-method"></a>Método IWMPPlaylist:: insertItem

O método **insertItem** insere um item de mídia em um local especificado em uma lista de reprodução.

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

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de base zero no qual o item de mídia será inserido na lista de reprodução.

</dd> <dt>

*pIWMPMedia* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPMedia** que representa o item de mídia a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens de mídia após o item inserido terão seus índices aumentados em um.

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





