---
title: Método ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardTypeMode define o modo de tipo para um teclado virtual.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardTypeMode
- Método SetSoftKeyboardTypeMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455644"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a>Método ISoftKbd:: SetSoftKeyboardTypeMode

O método **ISoftKbd:: SetSoftKeyboardTypeMode** define o modo de tipo para um teclado virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tipo de* \[ no\]
</dt> <dd>

O modo de tipo. Os valores possíveis são definidos para a enumeração [**typemode**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *typemode* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[**TIPO de**](typemode.md)
</dt> </dl>

 

 





