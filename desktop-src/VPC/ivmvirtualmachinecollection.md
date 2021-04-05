---
title: Interface IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Define a coleção de máquinas virtuais no Windows Virtual PC. Para obter um objeto IVMVirtualMachineCollection, use a propriedade IVMVirtualPC VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Virtual PC de interface IVMVirtualMachineCollection
- Virtual PC de interface IVMVirtualMachineCollection, descrito
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086211"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interface IVMVirtualMachineCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de máquinas virtuais no Windows Virtual PC. Para obter um objeto **IVMVirtualMachineCollection** , use a propriedade [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membros

A interface **IVMVirtualMachineCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMVirtualMachineCollection** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso          | Descrição                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                   |
| [**Contar**](ivmvirtualmachinecollection-count.md)<br/>        | Somente leitura<br/> | O número de máquinas virtuais nesta coleção.<br/>                  |
| [**Item**](ivmvirtualmachinecollection-item.md)<br/>          | Somente leitura<br/> | O objeto de máquina virtual que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection é definido como 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

