---
title: Interface IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Define a coleção de portas paralelas na máquina virtual. Para obter um objeto IVMParallelPortCollection, use a propriedade IVMVirtualMachine ParallelPorts.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Virtual PC de interface IVMParallelPortCollection
- Virtual PC de interface IVMParallelPortCollection, descrito
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086346"
---
# <a name="ivmparallelportcollection-interface"></a>Interface IVMParallelPortCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de portas paralelas na máquina virtual. Para obter um objeto **IVMParallelPortCollection** , use a propriedade [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membros

A interface **IVMParallelPortCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPortCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMParallelPortCollection** tem essas propriedades.



| Propriedade                                                           | Tipo de acesso          | Descrição                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmparallelportcollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                 |
| [**Contar**](ivmparallelportcollection-count.md)<br/>        | Somente leitura<br/> | O número de portas paralelas nesta coleção.<br/>                  |
| [**Item**](ivmparallelportcollection-item.md)<br/>          | Somente leitura<br/> | O objeto de porta paralela que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMVirtualMachine::P arallelPorts**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

