---
title: Propriedade de item IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Objeto IVMVirtualNetwork que corresponde ao índice especificado.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009460"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a>Propriedade IVMVirtualNetworkCollection:: item

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                                      |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro *virtualNetwork* é **NULL**.<br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualNetworkCollection é definido como 8ed680be-4242-4B2A-a21c-1982d8b0f675<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> <dt>

[**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

