---
title: Interface IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Define uma coleção de unidades de disquete na máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Virtual PC de interface IVMFloppyDriveCollection
- Virtual PC de interface IVMFloppyDriveCollection, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369906"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interface IVMFloppyDriveCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma coleção de unidades de disquete na máquina virtual. Para obter um objeto **IVMFloppyDriveCollection** , use a propriedade [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .

## <a name="members"></a>Membros

A interface **IVMFloppyDriveCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMFloppyDriveCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMFloppyDriveCollection** tem essas propriedades.



| Propriedade                                                          | Tipo de acesso          | Descrição                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                |
| [**Contar**](ivmfloppydrivecollection-count.md)<br/>        | Somente leitura<br/> | O número de unidades de disquete nesta coleção.<br/>                  |
| [**Item**](ivmfloppydrivecollection-item.md)<br/>          | Somente leitura<br/> | O objeto da unidade de disquete que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85CE-3cc93a925516<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

