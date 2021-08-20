---
title: Método IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces.h)
description: Recebe uma notificação de que uma máquina virtual tem falha tripla.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Computador Virtual do método OnTripleFault
- Método OnTripleFault pc virtual, interface IVMVirtualMachineEvents
- INTERFACE IVMVirtualMachineEvents pc virtual , método OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9328ceff18256621a590bf0f235aca8ff12b142e4cdedf389d9d270bfde9bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122686"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a>Método IVMVirtualMachineEvents::OnTripleFault

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que uma máquina virtual tem falha tripla.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é chamado quando uma máquina virtual tem falha tripla. O programa cliente deve implementar esse método de interface para receber notificação do evento TripleFault vmVirtualMachineEvent originado \_ de [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

