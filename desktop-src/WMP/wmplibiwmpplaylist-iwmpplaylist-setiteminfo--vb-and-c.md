---
title: Método IWMPPlaylist setItemInfo
description: O método setItemInfo define o valor de um atributo da playlist atual.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Windows Media Player do método setItemInfo
- método setItemInfo Windows Media Player, interface IWMPPlaylist
- Windows Media Player de interface IWMPPlaylist, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcd4bf2d90b90a825942c5634b2b2cde3bb82e7806fe62ecd5e7d298cd191997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568701"
---
# <a name="iwmpplaylistsetiteminfo-method"></a>Método IWMPPlaylist:: setItemInfo

O método **setItemInfo** define o valor de um atributo da playlist atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do atributo.

</dd> <dt>

*bstrvalue* \[ no\]
</dt> <dd>

Um **System. String** que é o valor do atributo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, você deve ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Consulte a propriedade [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obter o código de exemplo que usa essa propriedade.

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

[**IWMPPlaylist. getItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





