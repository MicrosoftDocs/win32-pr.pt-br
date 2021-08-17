---
title: Propriedade NetworkAddresses IVMHostInfo (VPCCOMInterfaces.h)
description: Recupera uma coleção enumerável de endereços TCP/IP no computador host.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- NetworkAddresses propriedade Pc Virtual
- Propriedade NetworkAddresses Pc Virtual , interface IVMHostInfo
- INTERFACE IVMHostInfo pc virtual , propriedade NetworkAddresses
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAddresses
- IVMHostInfo.get_NetworkAddresses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b3be88d65e567fd9586ae9f0a205eb2c55c77328d7725f59e5c80a8e63324b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753288"
---
# <a name="ivmhostinfonetworkaddresses-property"></a>Propriedade IVMHostInfo::NetworkAddresses

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma coleção enumerável de endereços TCP/IP no computador host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a>Valor da propriedade

Uma matriz de endereços TCP/IP, em notação decimal pontilhada.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo é definido como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

