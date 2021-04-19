---
title: Interface IVMParallelPort (VPCCOMInterfaces. h)
description: Define uma porta paralela dentro de uma máquina virtual.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Virtual PC de interface IVMParallelPort
- Virtual PC de interface IVMParallelPort, descrito
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797518"
---
# <a name="ivmparallelport-interface"></a>Interface IVMParallelPort

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma porta paralela dentro de uma máquina virtual. Essa interface permite que você configure portas paralelas dentro de uma máquina virtual. Você pode recuperar um objeto **IVMParallelPort** do objeto [**IVMParallelPortCollection**](ivmparallelportcollection.md) retornado da propriedade [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membros

A interface **IVMParallelPort** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPort** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMParallelPort** tem esses métodos.



| Método                              | Descrição                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_ID**](ivmparallelport--id.md) | Recupera o identificador interno da porta paralela.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMParallelPort** tem essas propriedades.



| Propriedade                                        | Tipo de acesso           | Descrição                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Nome**](ivmparallelport-name.md)<br/> | Leitura/gravação<br/> | O nome da porta paralela.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort é definido como 097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



 

