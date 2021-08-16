---
title: Método ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc.h)
description: O método ISoftKbd UnadviseSoftKeyboardEventSink remove um sink de evento de teclado flexível.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Método UnadviseSoftKeyboardEventSink Estrutura de Serviços de Texto
- Método UnadviseSoftKeyboardEventSink Estrutura de Serviços de Texto , interface ISoftKbd
- Interface ISoftKbd Estrutura de Serviços de Texto , método UnadviseSoftKeyboardEventSink
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
ms.openlocfilehash: 90552c09e47d8a51f413f0588b12c8da5d44e665a6a5a51a79dc31717c6d56c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877106"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a>Método ISoftKbd::UnadviseSoftKeyboardEventSink

O **método ISoftKbd::UnadviseSoftKeyboardEventSink** remove um sink de evento de teclado flexível.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tid* \[ Em\]
</dt> <dd>

Identificador do cliente que possui o sink de eventos do teclado suave. Esse valor foi passado quando o sink do evento foi instalado usando [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                                   | Descrição                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | O método foi bem-sucedido.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | O *parâmetro tid* é inválido.<br/>                    |
| <dl> <dt>**CONNECT \_ E \_ NOCONNECTION**</dt> </dl> | O sink de consultoria identificado *por tid* não foi encontrado.<br/> |



 

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

[ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





