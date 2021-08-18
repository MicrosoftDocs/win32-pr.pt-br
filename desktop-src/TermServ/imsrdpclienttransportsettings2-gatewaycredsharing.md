---
title: Propriedade IMsRdpClientTransportSettings2 GatewayCredSharing
description: Especifica ou recupera a configuração para se o recurso de compartilhamento de credenciais do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayCredSharing
- Propriedade GatewayCredSharing Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d489678006e842a6da82f5d2f9489f84a9a20fd70bfe8f18018aaa6d412c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974646"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Propriedade IMsRdpClientTransportSettings2:: GatewayCredSharing

Especifica ou recupera a configuração para se o recurso de compartilhamento de credenciais do gateway de Área de Trabalho Remota (Gateway RD) está habilitado. quando o recurso é habilitado, o Área de Trabalho Remota ActiveX controle tenta usar as mesmas credenciais para autenticar o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o servidor de Gateway de área de trabalho remota.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Valor da propriedade

Se definido como um, o compartilhamento de credenciais está habilitado. Se definido como zero, o compartilhamento de credenciais será desabilitado.

## <a name="error-codes"></a>Códigos do Erro

Retornará **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

essa propriedade é usada pelo controle de ActiveX para implementar um único prompt para o compartilhamento de credenciais entre o servidor de Host da Sessão RD e o servidor de Gateway de área de trabalho remota. O compartilhamento de credenciais não oferece suporte ao compartilhamento de senha baseado na Web com [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) ou [**clearTextPassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 





