---
title: Método ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardTypeMode recupera o modo de tipo para um teclado virtual.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardTypeMode
- Método GetSoftKeyboardTypeMode de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369199"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a>Método ISoftKbd:: GetSoftKeyboardTypeMode

O método **ISoftKbd:: GetSoftKeyboardTypeMode** recupera o modo de tipo para um teclado virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpTypeMode* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera o modo de tipo. Os valores possíveis são definidos para a enumeração [**typemode**](typemode.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro *lpTypeMode* é inválido.<br/> |



 

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

[**ISoftKbd::SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[**TIPO de**](typemode.md)
</dt> </dl>

 

 





