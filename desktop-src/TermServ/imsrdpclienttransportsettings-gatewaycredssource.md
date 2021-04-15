---
title: Propriedade IMsRdpClientTransportSettings GatewayCredsSource
description: Especifica ou recupera o método de autenticação do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayCredsSource
- Propriedade GatewayCredsSource Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings, Propriedade GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369374"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>Propriedade IMsRdpClientTransportSettings:: GatewayCredsSource

Especifica ou recupera o método de autenticação do gateway de Área de Trabalho Remota (Gateway RD).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **ULONG** que especifica o método de autenticação de gateway de área de trabalho remota. Esse parâmetro pode usar um dos valores a seguir.

<dt>

\_ \_ Modo de credenciais de proxy de TSC \_ \_ userpass (0)
</dt> <dd>

Use uma senha (NTLM) como o método de autenticação para o gateway de área de trabalho remota.

</dd> <dt>

\_ \_ \_ \_ Cartão inteligente de credenciais de proxy de TSC (1)
</dt> <dd>

Use um cartão inteligente como o método de autenticação para o Gateway RD.

</dd> <dt>

\_ \_ \_ Modo de credenciais de proxy \_ de TSC Any (4)
</dt> <dd>

Use qualquer método de autenticação para o Gateway RD.

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings é definido como 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





