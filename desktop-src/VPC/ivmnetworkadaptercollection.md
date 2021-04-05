---
title: Interface IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Define uma coleção de placas de interface de rede virtual. Para obter um objeto IVMNetworkAdapterCollection, use as propriedades IVMVirtualMachine adaptadores, IVMVirtualNetwork adaptadores e IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Virtual PC de interface IVMNetworkAdapterCollection
- Virtual PC de interface IVMNetworkAdapterCollection, descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009466"
---
# <a name="ivmnetworkadaptercollection-interface"></a>Interface IVMNetworkAdapterCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma coleção de placas de interface de rede virtual. Para obter um objeto IVMNetworkAdapterCollection, use as propriedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)e [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .

## <a name="members"></a>Membros

A interface **IVMNetworkAdapterCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMNetworkAdapterCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMNetworkAdapterCollection** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso          | Descrição                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmnetworkadaptercollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                                                  |
| [**Contar**](ivmnetworkadaptercollection-count.md)<br/>        | Somente leitura<br/> | O número de interfaces de rede nesta coleção.<br/>                                               |
| [**Item**](ivmnetworkadaptercollection-item.md)<br/>          | Somente leitura<br/> | O objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-EBCD-47CF-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

