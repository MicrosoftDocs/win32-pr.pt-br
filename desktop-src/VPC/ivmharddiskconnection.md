---
title: Interface IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Define a conexão para um disco rígido dentro da máquina virtual.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtual PC de interface IVMHardDiskConnection
- Virtual PC de interface IVMHardDiskConnection, descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763807"
---
# <a name="ivmharddiskconnection-interface"></a>Interface IVMHardDiskConnection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a conexão para um disco rígido dentro da máquina virtual. Um objeto **IVMHardDiskConnection** é retornado do método [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) . Você também pode recuperar um objeto **IVMHardDiskConnection** do objeto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) retornado da propriedade [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membros

A interface **IVMHardDiskConnection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnection** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMHardDiskConnection** tem esses métodos.



| Método                                                         | Descrição                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [**SetBusLocation**](ivmharddiskconnection-setbuslocation.md) | Define o local do barramento ao qual este disco rígido está anexado.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMHardDiskConnection** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso          | Descrição                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [**BusNumber**](ivmharddiskconnection-busnumber.md)<br/>       | Somente leitura<br/> | O número do barramento ao qual a imagem da unidade está anexada.<br/>                   |
| [**DeviceNumber**](ivmharddiskconnection-devicenumber.md)<br/> | Somente leitura<br/> | O número do dispositivo ao qual a imagem da unidade está anexada.<br/>                |
| [**HD**](ivmharddiskconnection-harddisk.md)<br/>         | Somente leitura<br/> | Um objeto de disco rígido correspondente a essa conexão.<br/>                   |
| [**UndoHardDisk**](ivmharddiskconnection-undoharddisk.md)<br/> | Somente leitura<br/> | Um objeto de disco rígido correspondente à imagem de desfazer disco da conexão.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



 

