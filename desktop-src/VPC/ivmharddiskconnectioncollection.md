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
ms.openlocfilehash: 997cbe915e7e4addac60c639a7ee6c260f07271ff5981939b25dbefd49fcba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345700"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interface IVMHardDiskConnectionCollection

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de conexões de disco rígido na máquina virtual. Para obter um objeto **IVMHardDiskConnectionCollection** , use a propriedade [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membros

A interface **IVMHardDiskConnectionCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnectionCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMHardDiskConnectionCollection** tem essas propriedades.



| Propriedade                                                                 | Tipo de acesso          | Descrição                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                        |
| [**Contagem**](ivmharddiskconnectioncollection-count.md)<br/>        | Somente leitura<br/> | O número de conexões de disco rígido nesta coleção.<br/>                  |
| [**Item**](ivmharddiskconnectioncollection-item.md)<br/>          | Somente leitura<br/> | O objeto de conexão de disco rígido que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                               |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection é definido como b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

