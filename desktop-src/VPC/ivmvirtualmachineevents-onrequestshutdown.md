---
title: Método IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Recebe a notificação de que uma solicitação de desligamento foi feita.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- OnRequestShutdown do método virtual PC
- Método OnRequestShutdown Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929c9a293e760a12ace62766cbd7a0c016980fc2399cdde494402a272d90fe0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123166"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>Método IVMVirtualMachineEvents:: OnRequestShutdown

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que uma solicitação de desligamento foi feita.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado sempre que a sessão da máquina virtual está prestes a ser desligada. O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualMachineEvent \_ RequestShutdown** originado do [**IVMVirtualMachine**](ivmvirtualmachine.md).

Essa notificação de evento é enviada somente quando a sessão de máquinas virtuais está prestes a ser desligada. As rotinas de desligamento do sistema operacional, como [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), não acionam esse evento diretamente, a menos que eles também tentem realizar uma desligamento do software do hardware virtual.

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

 

