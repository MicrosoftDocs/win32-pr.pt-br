---
title: Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces.h)
description: Recebe uma notificação de que o estado de uma máquina virtual foi alterado. | Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces.h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Computador Virtual do método OnStateChange
- Método OnStateChange Pc Virtual , interface IVMVirtualMachineEvents
- INTERFACE IVMVirtualMachineEvents pc virtual , método OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf966d2439f3095051331b5412bc92cca9ba76e6f98c9777402ba449f2e7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122696"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>Método IVMVirtualMachineEvents::OnStateChange

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que o estado de uma máquina virtual foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualMachineState* \[ Em\]
</dt> <dd>

O novo estado da máquina virtual. Para ver uma lista de valores, [**consulte VMVMState.**](vmvmstate.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é chamado quando o estado dessa máquina virtual muda. O programa cliente deve implementar esse método de interface para receber notificação do evento stateChanged vmVirtualMachineEvent originado \_ de [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

