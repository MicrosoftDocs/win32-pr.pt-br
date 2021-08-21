---
title: Método IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces.h)
description: Recebe uma notificação de que um disco necessário para uma VM tem pouco espaço livre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Computador Virtual do método OnDiskOutOfSpace
- Computador Virtual do método OnDiskOutOfSpace, interface IVMVirtualMachineEvents
- INTERFACE IVMVirtualMachineEvents pc virtual , método OnDiskOutOfSpace
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
ms.openlocfilehash: c482f0a713fda7e13436dc28d295469237273a7c607e522ce457ec908f210223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056624"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>Método IVMVirtualMachineEvents::OnDiskOutOfSpace

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que um disco necessário para uma VM (máquina virtual) tem pouco espaço livre. Se o espaço livre cair abaixo de 100 MB, esse evento será recebido como um aviso e se o espaço livre cair abaixo de 20 MB, esse evento será recebido novamente como um erro e a VM será pausada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*criticallyLow* \[ Em\]
</dt> <dd>

Definido como **VARIANT \_ TRUE** se o disco tiver menos de 20 MB livres e como **VARIANT \_ FALSE** se o espaço livre for maior que 20 MB, mas menor que 100 MB.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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

 

