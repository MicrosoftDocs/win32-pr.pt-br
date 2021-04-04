---
title: Propriedade IVMNetworkAdapter IsEthernetAddressDynamic (VPCCOMInterfaces. h)
description: Determina se o endereço Ethernet é gerado dinamicamente.
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- Propriedade IsEthernetAddressDynamic Virtual PC
- Propriedade IsEthernetAddressDynamic Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade IsEthernetAddressDynamic
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008808"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a>Propriedade IVMNetworkAdapter:: IsEthernetAddressDynamic

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se o endereço Ethernet é gerado dinamicamente.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a>Valor da propriedade

Defina como VARIANT \_ true se o endereço Ethernet deve ser gerado dinamicamente e Variant \_ false se o endereço Ethernet for estático.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                                                                                                             |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                                                                                                                                |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A máquina virtual não foi encontrada. Isso poderá ocorrer se o computador tiver sido removido após a criação do objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                                                                                         |



## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida como **true** (padrão) para a maioria das interfaces de rede virtual. Se o software no convidado exigir um endereço Ethernet estático, essa propriedade deverá ser definida como **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

