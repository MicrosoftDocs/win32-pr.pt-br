---
title: Método isidêntico IWMPLibrary
description: O método isidêntico retorna um valor que indica se o objeto fornecido é o mesmo que o atual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- método isidêntico Windows Media Player
- método isidêntico Windows Media Player, interface IWMPLibrary
- Windows Media Player de interface IWMPLibrary, método isidêntico
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506046"
---
# <a name="iwmplibraryisidentical-method"></a>Método IWMPLibrary:: isidêntico

O método **isidêntico** retorna um valor que indica se o objeto fornecido é o mesmo que o atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIWMPLibrary* \[ no\]
</dt> <dd>

Uma interface **WMPLib. IWMPLibrary** que representa o objeto a ser comparado com o atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System. Boolean** que é o resultado da comparação. O valor **true** indica que os objetos são os mesmos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





