---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Recebe uma notificação de que o Windows Virtual PC registra um evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- OnEventLogged do método virtual PC
- Método OnEventLogged Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface virtual PC, método OnEventLogged
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
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499450"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>Método IVMVirtualPCEvents:: OnEventLogged

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que o Windows Virtual PC registra um evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*logMessageID* \[ no\]
</dt> <dd>

O identificador de mensagem da mensagem de log de eventos que foi registrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando o Windows Virtual PC registra uma mensagem no log de eventos do Windows. O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualPCEvent \_ EventLogged** originado do [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41F7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

