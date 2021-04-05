---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: O método ISoftKbd UnadviseSoftKeyboardEventSink remove um coletor de eventos de teclado flexível.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Estrutura de serviços de texto do método UnadviseSoftKeyboardEventSink
- Método UnadviseSoftKeyboardEventSink de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644971"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>Método ISoftKbd:: UnadviseSoftKeyboardEventSink

O método **ISoftKbd:: UnadviseSoftKeyboardEventSink** remove um coletor de eventos de teclado flexível.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tid* \[ no\]
</dt> <dd>

Identificador do cliente que possui o coletor de eventos de teclado virtual. Esse valor foi passado quando o coletor de eventos foi instalado usando [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                                   | Descrição                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | O método foi bem-sucedido.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | O parâmetro *tid* é inválido.<br/>                    |
| <dl> <dt>**CONECTAR \_ E \_ noconnection**</dt> </dl> | O coletor de aviso identificado pelo *tid* não foi encontrado.<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





