---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: O método ISoftKbd AdviseSoftKeyboardEventSink instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Estrutura de serviços de texto do método AdviseSoftKeyboardEventSink
- Método AdviseSoftKeyboardEventSink de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369811"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>Método ISoftKbd:: AdviseSoftKeyboardEventSink

O método **ISoftKbd:: AdviseSoftKeyboardEventSink** instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwKeyboardId* \[ no\]
</dt> <dd>

Identificador do teclado virtual.

</dd> <dt>

*riid* \[ no\]
</dt> <dd>

Identificador de interface para a interface do coletor.

</dd> <dt>

*punk* \[ no\]
</dt> <dd>

Ponteiro para [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface do coletor especificada por *riid*. Este parâmetro não pode ser definido como **nulo**.

</dd> <dt>

*pdwCookie* \[ fora\]
</dt> <dd>

Ponteiro para o buffer no qual esse método recupera o "cookie" do teclado virtual usado para conexão com o cliente. O cookie deve ser exclusivo para cada conexão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais parâmetros são inválidos.<br/> |



 

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

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

