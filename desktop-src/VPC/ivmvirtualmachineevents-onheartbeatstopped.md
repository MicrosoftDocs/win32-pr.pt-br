---
title: Método IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- OnHeartbeatStopped do método virtual PC
- Método OnHeartbeatStopped Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad4af982899f2f5f5dce6d78569323fbb6a85168c81b7c88c3ee0c62b3a39f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056583"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a>Método IVMVirtualMachineEvents:: OnHeartbeatStopped

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando o sistema operacional convidado para esta máquina virtual foi interrompido abruptamente. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent HeartbeatStopped originado do [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

