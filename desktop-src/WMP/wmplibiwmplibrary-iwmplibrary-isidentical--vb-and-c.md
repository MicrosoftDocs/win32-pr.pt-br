---
title: Método isidêntico IWMPLibrary
description: O método isidêntico retorna um valor que indica se o objeto fornecido é o mesmo que o atual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- método isidêntico do Windows Media Player
- método isidêntico Windows Media Player, interface IWMPLibrary
- Interface IWMPLibrary do Windows Media Player, método isidêntico
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
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764522"
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

## <a name="return-value"></a>Retornar valor

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

 

 





