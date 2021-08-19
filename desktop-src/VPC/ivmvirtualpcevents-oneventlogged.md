---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces.h)
description: Recebe uma notificação de que Windows pc virtual registra um evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Computador Virtual do método OnEventLogged
- Computador Virtual do método OnEventLogged, interface IVMVirtualPCEvents
- INTERFACE IVMVirtualPCEvents pc virtual , método OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998516"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Método IVMVirtualPCEvents::OnEventLogged

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que Windows pc virtual registra um evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*logMessageID* \[ Em\]
</dt> <dd>

O identificador de mensagem da mensagem de log de eventos registrada em log.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é chamado quando Windows computador virtual registra uma mensagem no log Windows eventos. O programa cliente deve implementar esse método de interface para receber notificação do evento **\_ EventLogged vmVirtualPCEvent** originado de [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

