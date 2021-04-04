---
title: Método IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Recebe uma notificação de que um disco necessário para uma VM está com pouco espaço livre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- OnDiskOutOfSpace do método virtual PC
- Método OnDiskOutOfSpace Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824139"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>Método IVMVirtualMachineEvents:: OnDiskOutOfSpace

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que um disco necessário para uma VM (máquina virtual) está com pouco espaço livre. Se o espaço livre cair abaixo de 100 MB, esse evento será recebido como um aviso e, se o espaço livre cair abaixo de 20 MB, esse evento será recebido novamente como um erro e a VM será pausada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*criticallyLow* \[ no\]
</dt> <dd>

Defina como **Variant \_ true** se o disco tiver menos de 20 MB livres e para a **variante \_ false** se o espaço livre for superior a 20 MB, mas menor que 100 MB.

</dd> </dl>

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

 

