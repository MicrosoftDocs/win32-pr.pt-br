---
title: Propriedade IMsRdpClientNonScriptable3 NegotiateSecurityLayer
description: Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient5
- Objeto MsRdpClient5 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient6
- Objeto MsRdpClient6 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient7
- Objeto MsRdpClient7 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient8
- Objeto MsRdpClient8 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
- Propriedade NegotiateSecurityLayer Serviços de Área de Trabalho Remota, objeto MsRdpClient9
- Objeto MsRdpClient9 Serviços de Área de Trabalho Remota, Propriedade NegotiateSecurityLayer
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
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781022"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Propriedade IMsRdpClientNonScriptable3:: NegotiateSecurityLayer

Especifica ou recupera se a camada de segurança de negociação está habilitada para a conexão.

Esta propriedade é de leitura/gravação.

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

Se essa propriedade for definida como **Variant \_ FALSE** e autenticação no nível da rede (NLA) estiver habilitada no sistema operacional do cliente, o cliente não negociará a camada de segurança e, em vez disso, usará o NLA para proteger a conexão RDP. Se essa propriedade for definida como **Variant \_ true**, o cliente negociará entre a NLA e a segurança de RDP básica.

> [!Note]  
> A desabilitação da negociação da camada de segurança só é possível ao se conectar a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) que executa o Windows Vista ou sistemas operacionais posteriores. Se essa propriedade estiver habilitada e o cliente tentar se conectar a um servidor de Host da Sessão RD que executa um sistema operacional anterior, a conexão falhará.

 

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

 

 





