---
title: Propriedade IVMNetworkAdapter EthernetAddress (VPCCOMInterfaces. h)
description: Endereço Ethernet (MAC) da interface de rede.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Propriedade EthernetAddress Virtual PC
- Propriedade EthernetAddress Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644214"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>Propriedade IVMNetworkAdapter:: EthernetAddress

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o endereço Ethernet (MAC) da interface de rede.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço MAC da NIC virtual. Ele deve ter o formato "*XX* - *XX* XX XX XX XX -  -  -  - ", em que cada *X* é um dígito hexadecimal.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>                                                                                                   | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                              | O parâmetro é **NULL**.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                           | O parâmetro não está no formato correto.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>VM \_ E não é possível \_ \_ definir o \_ \_ \_ endereço MAC dinâmico</dt> <dt>0xA004070A</dt> </dl> | O endereço Ethernet para uma interface de rede pode ser gerado dinamicamente ou pode ser definido como um endereço estático pelo usuário. Este método não pode ser chamado quando o endereço está definido para ser gerado dinamicamente. A propriedade [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) é usada para alterar o comportamento de geração do endereço Ethernet.<br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>                      | A máquina virtual não foi encontrada. Isso poderá ocorrer se o computador tiver sido removido após a criação do objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                      | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

