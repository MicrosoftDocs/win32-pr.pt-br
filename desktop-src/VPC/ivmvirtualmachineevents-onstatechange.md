---
title: Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Recebe a notificação de que o estado de uma máquina virtual foi alterado. | Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- OnStateChange do método virtual PC
- Método OnStateChange Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnStateChange
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
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298413"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>Método IVMVirtualMachineEvents:: OnStateChange

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que o estado de uma máquina virtual foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualMachineState* \[ no\]
</dt> <dd>

O novo estado da máquina virtual. Para obter uma lista de valores, consulte [**VMVMState**](vmvmstate.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando o estado dessa máquina virtual é alterado. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent StateChanged originado de [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

