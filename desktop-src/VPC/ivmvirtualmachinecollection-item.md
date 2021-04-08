---
title: Propriedade de item IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de máquina virtual que corresponde ao índice especificado.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008802"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a>Propriedade IVMVirtualMachineCollection:: item

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto de máquina virtual que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida. <br/>                                                      |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro *VirtualMachine* é **nulo**. <br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção. <br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection é definido como 59f31786-2a3d-4fbf-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

