---
title: Interface IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Define uma coleção de objetos IVMVirtualNetwork. Para obter um objeto IVMVirtualNetworkCollection, use a propriedade IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Virtual PC de interface IVMVirtualNetworkCollection
- Virtual PC de interface IVMVirtualNetworkCollection, descrito
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645045"
---
# <a name="ivmvirtualnetworkcollection-interface"></a>Interface IVMVirtualNetworkCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define uma coleção de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) . Para obter um objeto **IVMVirtualNetworkCollection** , use a propriedade [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .

## <a name="members"></a>Membros

A interface **IVMVirtualNetworkCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualNetworkCollection** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IVMVirtualNetworkCollection** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso          | Descrição                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualnetworkcollection--newenum.md)<br/> | Somente leitura<br/> | Um enumerador para a coleção.<br/>                                                                  |
| [**Contar**](ivmvirtualnetworkcollection-count.md)<br/>        | Somente leitura<br/> | O número de redes virtuais nesta coleção.<br/>                                                 |
| [**Item**](ivmvirtualnetworkcollection-item.md)<br/>          | Somente leitura<br/> | O objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde ao índice especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection é definido como 8ed680be-4242-4B2A-a21c-1982d8b0f675<br/> |



 

