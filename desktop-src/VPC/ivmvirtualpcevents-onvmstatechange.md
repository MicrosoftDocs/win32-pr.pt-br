---
title: Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Recebe a notificação de que o estado de uma máquina virtual foi alterado. | Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- OnVMStateChange do método virtual PC
- Método OnVMStateChange Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface virtual PC, método OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811417"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>Método IVMVirtualPCEvents:: OnVMStateChange

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que o estado de uma máquina virtual foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualMachineConfig* \[ no\]
</dt> <dd>

O nome da máquina virtual.

</dd> <dt>

*virtualMachineState* \[ no\]
</dt> <dd>

O novo estado da máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualPCEvent \_ VMStateChanged** originado do [**IVMVirtualPC**](ivmvirtualpc.md). Para monitorar uma máquina virtual específica, use o método [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .

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

 

