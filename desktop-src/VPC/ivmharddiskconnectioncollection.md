---
title: Interface IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Define a coleção de conexões de disco rígido na máquina virtual. Para obter um objeto IVMHardDiskConnectionCollection, use a propriedade IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Virtual PC de interface IVMHardDiskConnectionCollection
- Virtual PC de interface IVMHardDiskConnectionCollection, descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454585"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interface IVMHardDiskConnectionCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de conexões de disco rígido na máquina virtual. Para obter um objeto **IVMHardDiskConnectionCollection** , use a propriedade [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membros

A interface **IVMHardDiskConnectionCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnectionCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMHardDiskConnectionCollection** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                        |
| [**Contar**](ivmharddiskconnectioncollection-count.md)<br/>        | Somente leitura<br/> | O número de conexões de disco rígido nesta coleção.<br/>                  |
| [**Item**](ivmharddiskconnectioncollection-item.md)<br/>          | Somente leitura<br/> | O objeto de conexão de disco rígido que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                               |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                      |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection é definido como b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

