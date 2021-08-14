---
title: Método isidêntico IWMPStringCollection2
description: O método isidêntico retorna um valor que indica se o objeto representado pela interface fornecida é o mesmo que o atual.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- método isidêntico Windows Media Player
- método isidêntico Windows Media Player, interface IWMPStringCollection2
- Windows Media Player de interface IWMPStringCollection2, método isidêntico
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4576522c1b6d6834ded5e100a2618dcb45204f887420968a5828fdc5c9bd0fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330900"
---
# <a name="iwmpstringcollection2isidentical-method"></a>Método IWMPStringCollection2:: isidêntico

O método **isidêntico** retorna um valor que indica se o objeto representado pela interface fornecida é o mesmo que o atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIWMPStringCollection2* \[ no\]
</dt> <dd>

A interface **WMPLib. IWMPStringCollection2** que representa o objeto a ser comparado com o atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **System. Boolean** que é o resultado da comparação. Um valor **true** indica que os objetos da coleção de cadeia de caracteres são os mesmos.

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





