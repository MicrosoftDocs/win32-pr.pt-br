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
ms.openlocfilehash: 89fa3df8431f829c0dd85cd3a448965e98b4e6d5e6285ae75d18c76257ddbb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000906"
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

 

 





