---
title: Interface IVMFloppyDriveCollection (VPCCOMInterfaces.h)
description: Define uma coleção de unidades de disquete dentro da máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- IVMFloppyDriveCollection interface Virtual PC
- INTERFACE IVMFloppyDriveCollection pc virtual , descrito
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
ms.openlocfilehash: 6637c0c4a8c8b87f4458081b0893b0939c8eaf04c97738c02d39da5e0fd8eebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653586"
---
# <a name="ivmfloppydrivecollection-interface"></a>Interface IVMFloppyDriveCollection

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma coleção de unidades de disquete dentro da máquina virtual. Para obter um **objeto IVMFloppyDriveCollection,** use a [**propriedade IVMVirtualMachine::FloppyDrives.**](ivmvirtualmachine-floppydrives.md)

## <a name="members"></a>Membros

A interface **IVMFloppyDriveCollection** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMFloppyDriveCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMFloppyDriveCollection** tem essas propriedades.



| Propriedade                                                          | Tipo de acesso          | Descrição                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                |
| [**Contagem**](ivmfloppydrivecollection-count.md)<br/>        | Somente leitura<br/> | O número de unidades de disquete nesta coleção.<br/>                  |
| [**Item**](ivmfloppydrivecollection-item.md)<br/>          | Somente leitura<br/> | O objeto de unidade de disquete que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

