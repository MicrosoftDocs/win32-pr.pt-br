---
title: Propriedade EthernetAddress IVMNetworkAdapter (VPCCOMInterfaces.h)
description: Endereço Ethernet (MAC) do interface de rede.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Propriedade EthernetAddress Pc Virtual
- Propriedade EthernetAddress Pc Virtual, interface IVMNetworkAdapter
- INTERFACE IVMNetworkAdapter pc virtual, propriedade EthernetAddress
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
ms.openlocfilehash: 3547bab24fdbaa50360a7198c020bb1dbc39b9efb9a1defad993a5be7a70fabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844034"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a>Propriedade IVMNetworkAdapter::EthernetAddress

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o endereço Ethernet (MAC) do interface de rede.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço MAC da NIC virtual. Ele deve ter o formato "*XX* -  - *XX XX* - *XX* - *XX* XX - *"* em que cada *X* é um dígito hexadecimal.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>                                                                                                   | A operação foi bem-sucedida.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                              | O parâmetro é **NULL.**<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                           | O parâmetro não está no formato correto.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>VM \_ E \_ NÃO PODE DEFINIR \_ \_ \_ ENDEREÇOS MAC \_ DINÂMICOS</dt> <dt>0XA004070A</dt> </dl> | O endereço Ethernet para um interface de rede pode ser gerado dinamicamente ou pode ser definido como um endereço estático pelo usuário. Esse método não pode ser chamado quando o endereço está definido para ser gerado dinamicamente. A [**propriedade IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) é usada para alterar o comportamento de geração do endereço Ethernet.<br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                      | A máquina virtual não foi encontrada. Isso poderá ocorrer se o computador tiver sido removido após a criação do objeto [**IVMNetworkAdapter.**](ivmnetworkadapter.md)<br/>                                                                                                                                                                                                                        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                      | Ocorreu um erro inesperado.<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter é definido como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

