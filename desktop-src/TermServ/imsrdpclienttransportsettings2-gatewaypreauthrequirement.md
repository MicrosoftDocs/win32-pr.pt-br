---
title: Propriedade IMsRdpClientTransportSettings2 GatewayPreAuthRequirement
description: Especifica ou recupera a configuração para se o recurso de senha de uso único (OTP) do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade GatewayPreAuthRequirement
- Propriedade GatewayPreAuthRequirement Serviços de Área de Trabalho Remota, interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2, Propriedade GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499762"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a>Propriedade IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement

Especifica ou recupera a configuração para se o recurso de senha de uso único (OTP) do gateway de Área de Trabalho Remota (Gateway RD) está habilitado.

Quando a OTP está habilitada, o **GatewayPreAuthRequirement** tenta consultar o cookie de OTP do armazenamento de cookies da Internet usando a propriedade [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) . Se for bem-sucedido, o **GatewayPreAuthRequirement** enviará o cookie de OTP para o servidor de firewall (como o Microsoft Internet Security and Acceleration \[ ISA \] Server) para pré-autenticação.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a>Valor da propriedade

Se definido como 1, o recurso de OTP será habilitado. Se definido como 0, o recurso de OTP será desabilitado.

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

 

 





