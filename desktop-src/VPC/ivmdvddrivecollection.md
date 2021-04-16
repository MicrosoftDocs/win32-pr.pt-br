---
title: Interface IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Define a coleção de unidades de CD e DVD na máquina virtual. Para obter um objeto IVMDVDDriveCollection, use a propriedade IVMVirtualMachine DVDROMDrives.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Virtual PC de interface IVMDVDDriveCollection
- Virtual PC de interface IVMDVDDriveCollection, descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752418"
---
# <a name="ivmdvddrivecollection-interface"></a>Interface IVMDVDDriveCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de unidades de CD e DVD na máquina virtual. Para obter um objeto **IVMDVDDriveCollection** , use a propriedade [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .

## <a name="members"></a>Membros

A interface **IVMDVDDriveCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDVDDriveCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMDVDDriveCollection** tem essas propriedades.



| Propriedade                                                       | Tipo de acesso          | Descrição                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                   |
| [**Contar**](ivmdvddrivecollection-count.md)<br/>        | Somente leitura<br/> | O número de unidades de CD e DVD nesta coleção.<br/>                 |
| [**Item**](ivmdvddrivecollection-item.md)<br/>          | Somente leitura<br/> | O objeto da unidade de CD ou DVD que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine::D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

