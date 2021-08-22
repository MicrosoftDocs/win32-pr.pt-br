---
title: Método ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc.h)
description: O método ISoftKbd AdviseSoftKeyboardEventSink instala um sink de evento de teclado flexível para manipular notificações onKeySelection do teclado flexível.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Método AdviseSoftKeyboardEventSink Estrutura de Serviços de Texto
- Método AdviseSoftKeyboardEventSink Estrutura de Serviços de Texto , interface ISoftKbd
- Interface ISoftKbd Estrutura de Serviços de Texto , método AdviseSoftKeyboardEventSink
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
ms.openlocfilehash: 73a3a734e66bb319bb7e24b6ca3b27299f984f33b98772c1cc446c40e3f27426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877983"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a>Método ISoftKbd::AdviseSoftKeyboardEventSink

O **método ISoftKbd::AdviseSoftKeyboardEventSink** instala um sink de evento de teclado flexível para manipular notificações onKeySelection do teclado flexível.

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

*dwKeyboardId* \[ Em\]
</dt> <dd>

Identificador do teclado suave.

</dd> <dt>

*riid* \[ Em\]
</dt> <dd>

Identificador de interface para a interface do sink.

</dd> <dt>

*(201* \[ Em\]
</dt> <dd>

Ponteiro para [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para a interface de sink especificada por *riid.* Esse parâmetro não pode ser definido como **NULL.**

</dd> <dt>

*pdwCookie* \[ out\]
</dt> <dd>

Ponteiro para o buffer no qual esse método recupera o "cookie" do teclado suave usado para conexão com o cliente. O cookie deve ser exclusivo para cada conexão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

