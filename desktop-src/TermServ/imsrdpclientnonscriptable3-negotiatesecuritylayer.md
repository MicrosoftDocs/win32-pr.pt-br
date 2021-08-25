---
title: Propriedade IMsRdpClientNonScriptable3 NegotiateSecurityLayer
description: Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable3
- Interface IMsRdpClientNonScriptable3 Serviços de Área de Trabalho Remota propriedade NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable4
- Interface IMsRdpClientNonScriptable4 Serviços de Área de Trabalho Remota propriedade NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota , interface IMsRdpClientNonScriptable5
- Interface IMsRdpClientNonScriptable5 Serviços de Área de Trabalho Remota propriedade NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota objeto , MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota propriedade , NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota objeto , MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota propriedade , NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota objeto , MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota propriedade , NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota objeto , MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota propriedade , NegotiateSecurityLayer
- A propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota objeto , MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota propriedade , NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f87abb5323289e60e3d29fa93d5e858a9a755224e7161ba28970ef5ccb186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771546"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Propriedade IMsRdpClientNonScriptable3::NegotiateSecurityLayer

Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica se a negociação da camada de segurança deve ser habilitada.

## <a name="remarks"></a>Comentários

Se essa propriedade for definida como **VARIANT \_ FALSE** e Autenticação no Nível da Rede (NLA) estiver habilitada no sistema operacional cliente, o cliente não negociará a camada de segurança e, em vez disso, usará o NLA para proteger a conexão RDP. Se essa propriedade for definida como **VARIANT \_ TRUE,** o cliente negociará entre o NLA e a segurança básica do RDP.

> [!Note]  
> Desabilitar a negociação de camada de segurança só é possível ao se conectar a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) executando Windows Vista ou sistemas operacionais posteriores. Se essa propriedade estiver habilitada e o cliente tentar se conectar a um servidor Host da Sessão RD executando um sistema operacional anterior, a conexão falhará.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 é definido como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





