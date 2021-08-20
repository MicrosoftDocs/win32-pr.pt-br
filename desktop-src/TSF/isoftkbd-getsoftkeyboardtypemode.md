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
ms.openlocfilehash: ab1205f0d9f59e027db75d2df580917392c445e812425c714b1688ce784a68ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952573"
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

## <a name="return-value"></a>Valor retornado

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
| Redistribuível<br/>          | TSF 1,0 em Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
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

 

 





