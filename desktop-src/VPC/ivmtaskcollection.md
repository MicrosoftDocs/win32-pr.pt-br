---
title: Interface IVMTaskCollection (VPCCOMInterfaces. h)
description: Define a coleção de objetos de tarefa. Para obter um objeto IVMTaskCollection, use a propriedade IVMVirtualPC Tasks.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Virtual PC de interface IVMTaskCollection
- Virtual PC de interface IVMTaskCollection, descrito
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958796"
---
# <a name="ivmtaskcollection-interface"></a>Interface IVMTaskCollection

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a coleção de objetos de tarefa. Para obter um objeto **IVMTaskCollection** , use a propriedade [**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md) .

## <a name="members"></a>Membros

A interface **IVMTaskCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMTaskCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMTaskCollection** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso          | Descrição                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                        |
| [**Contagem**](ivmtaskcollection-count.md)<br/>        | Somente leitura<br/> | O número de tarefas nesta coleção.<br/>                  |
| [**Item**](ivmtaskcollection-item.md)<br/>          | Somente leitura<br/> | O objeto de tarefa que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection é definido como 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

