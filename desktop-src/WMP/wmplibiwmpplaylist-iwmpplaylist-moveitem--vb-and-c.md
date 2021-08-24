---
title: Método moveItem IWMPPlaylist
description: O método moveItem altera o local de um item de mídia na playlist.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Método moveItem Windows Media Player
- Método moveItem Windows Media Player , interface IWMPPlaylist
- Interface IWMPPlaylist Windows Media Player , método moveItem
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
ms.openlocfilehash: f9f2c4f2aa3d4478a114e405b1b40816fc1697c2c291c272aabc68db3813766d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760656"
---
# <a name="iwmpplaylistmoveitem-method"></a>Método IWMPPlaylist::moveItem

O **método moveItem** altera o local de um item de mídia na playlist.

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

*lIndexOld* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o índice original.

</dd> <dt>

*lIndexNew* \[ Em\]
</dt> <dd>

Um **System.Int32** que é o novo índice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Todos os itens após o item inserido terão seus números de índice aumentados em um.

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





