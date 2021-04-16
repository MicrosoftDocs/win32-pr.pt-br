---
title: Método IWMPPlaylist moveItem
description: O método moveItem altera o local de um item de mídia na lista de reprodução.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765266"
---
# <a name="iwmpplaylistmoveitem-method"></a>Método IWMPPlaylist:: moveItem

O método **moveItem** altera o local de um item de mídia na lista de reprodução.

## <a name="syntax"></a>Sintaxe


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lIndexOld* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice original.

</dd> <dt>

*lIndexNew* \[ no\]
</dt> <dd>

Um **System. Int32** que é o novo índice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens após o item inserido terão seus números de índice aumentados em um.

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





