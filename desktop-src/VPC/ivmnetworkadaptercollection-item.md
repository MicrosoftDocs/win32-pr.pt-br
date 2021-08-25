---
title: Propriedade de item IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Objeto IVMNetworkAdapter que corresponde ao índice especificado.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1c84eb28eb0af583fd18db21ef13c9345caf6c03838d0b11c2af0a80e164bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973964"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a>Propriedade IVMNetworkAdapterCollection:: item

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida. <br/>                                                      |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro *networkInterface* é **nulo**. <br/>                                      |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção. <br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-EBCD-47CF-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> <dt>

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

