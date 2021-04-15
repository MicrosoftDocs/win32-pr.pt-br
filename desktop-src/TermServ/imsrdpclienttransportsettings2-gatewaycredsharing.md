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
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454783"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Propriedade IMsRdpClientTransportSettings2:: GatewayCredSharing

Especifica ou recupera a configuração para se o recurso de compartilhamento de credenciais do gateway de Área de Trabalho Remota (Gateway RD) está habilitado. Quando o recurso está habilitado, o controle ActiveX Área de Trabalho Remota tenta usar as mesmas credenciais para autenticar o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o servidor de gateway de área de trabalho remota.

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

Essa propriedade é usada pelo controle ActiveX para implementar um único prompt para o compartilhamento de credenciais entre o servidor de Host da Sessão RD e o servidor de gateway de área de trabalho remota. O compartilhamento de credenciais não oferece suporte ao compartilhamento de senha baseado na Web com [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) ou [**clearTextPassword**](imstscnonscriptable-cleartextpassword.md).

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

 

 





