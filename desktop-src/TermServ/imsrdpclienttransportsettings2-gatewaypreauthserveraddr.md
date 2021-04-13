---
title: Propriedade IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr
description: Especifica ou recupera o endereço Web do servidor de pré-autenticação, que é usado para o recurso de senha única (OTP) do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayPreAuthServerAddr
- Propriedade GatewayPreAuthServerAddr Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369369"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a>Propriedade IMsRdpClientTransportSettings2:: GatewayPreAuthServerAddr

Especifica ou recupera o endereço Web do servidor de pré-autenticação, que é usado para o recurso de senha única (OTP) do gateway de Área de Trabalho Remota (Gateway RD).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a>Valor da propriedade

O endereço Web do servidor de pré-autenticação; por exemplo, o endereço Web do Microsoft Internet Security and Acceleration (ISA) Server. Especifique o endereço Web usando o formato "https://*hostname*. *Nomedodomínio*. com/*WebSiteName*"ou"*nome do host* https://. *Nomedodomínio*. com/*WebSiteName*".

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista com SP1<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4C73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





