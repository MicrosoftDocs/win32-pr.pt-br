---
title: Método IWMPStringCollection2 getItemInfo
description: O método getItemInfo retorna a cadeia de caracteres correspondente ao nome e ao índice de item da coleção de cadeias de caracteres especificados.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- Método getItemInfo Windows Media Player
- Método getItemInfo Windows Media Player interface , IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player , método getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3f5371d55384544e4135e702b686cc7ce36707d204529ca7a4e68a3734d8ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899836"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>Método IWMPStringCollection2::getItemInfo

O **método getItemInfo** retorna a cadeia de caracteres correspondente ao nome e ao índice de item da coleção de cadeias de caracteres especificados.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lCollectionIndex* \[ Em\]
</dt> <dd>

O **System.Int32 que** especifica o índice baseado em zero do item de coleção de cadeias de caracteres do qual obter o atributo.

</dd> <dt>

*bstrItemName* \[ Em\]
</dt> <dd>

O **System.String** que é o nome do atributo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **System.String que** é o nome do item de coleção de cadeias de caracteres. Para atributos cujo valor subjacente é **System.Boolean**, ele retorna a cadeia de caracteres "true" ou "false".

## <a name="remarks"></a>Comentários

Para recuperar atributos com vários valores e atributos com valores complexos, use o **método getItemInfoByType.**

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMPStringCollection2 Interface**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfoByType (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





