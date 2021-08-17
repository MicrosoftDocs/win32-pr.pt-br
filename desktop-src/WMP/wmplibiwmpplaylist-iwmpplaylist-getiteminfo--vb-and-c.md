---
title: Método IWMPPlaylist getItemInfo
description: O método getItemInfo retorna o valor de um atributo de playlist especificado pelo nome.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- Windows Media Player do método getItemInfo
- método getItemInfo Windows Media Player, interface IWMPPlaylist
- Windows Media Player de interface IWMPPlaylist, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e3ad24f12333dbc9db5baf977300d1755a9cecc60739504da05478d5acc48e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745748"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>Método IWMPPlaylist:: getItemInfo

O método **getItemInfo** retorna o valor de um atributo de playlist especificado pelo nome.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrname* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do atributo playlist.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System. String** que é o valor do atributo playlist.

## <a name="remarks"></a>Comentários

Antes de usar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

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

[**IWMPPlaylist. setItemInfo (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





