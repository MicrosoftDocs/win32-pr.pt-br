---
title: Método onconfigurationchanged IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Método onconfigurationchanged Virtual PC
- Método onconfigurationchanged Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método onconfigurationchanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056634"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>Método IVMVirtualMachineEvents:: onconfigurationchanged

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configKey* \[ no\]
</dt> <dd>

O valor dentro da configuração que foi alterada.

</dd> <dt>

*configData* \[ no\]
</dt> <dd>

O novo valor para a configuração.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando a configuração é alterada para esta máquina virtual. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent configurationchanged originado de [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

