---
title: Método IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces.h)
description: Recebe uma notificação de que o suporte de uma máquina virtual para o modo de vídeo aprimorado foi alterado.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- OnEnhancedVideoModeChanged método Virtual PC
- OnEnhancedVideoModeChanged método Virtual PC , interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC , método OnEnhancedVideoModeChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bcdee9db2cf4b37b40d0cc77d6592c5ca1552b0a59642a01c2fe84bf4f69f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056614"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>Método IVMVirtualMachineEvents::OnEnhancedVideoModeChanged

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que o suporte de uma máquina virtual para o modo de vídeo aprimorado foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*enhancedVideoMode* \[ Em\]
</dt> <dd>

Indica se o modo de vídeo aprimorado está disponível.

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

 

