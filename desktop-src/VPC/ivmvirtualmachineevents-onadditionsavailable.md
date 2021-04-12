---
title: Método IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces. h)
description: Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- OnAdditionsAvailable do método virtual PC
- Método OnAdditionsAvailable Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnAdditionsAvailable
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455798"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a>Método IVMVirtualMachineEvents:: OnAdditionsAvailable

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

 

