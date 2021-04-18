---
title: Interface IMsRdpClientTransportSettings2
description: Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). | Interface IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings2
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings2, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780100"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interface IMsRdpClientTransportSettings2

Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="members"></a>Membros

A interface **IMsRdpClientTransportSettings2** herda de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientTransportSettings2** tem essas propriedades.



| Propriedade                                                                                                    | Tipo de acesso           | Descrição                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Leitura/gravação<br/> | Indica se o recurso de logon único para o gateway de área de trabalho remota está habilitado.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Leitura/gravação<br/> | O nome de domínio que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Leitura/gravação<br/> | O cookie de OTP criptografado.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Leitura/gravação<br/> | O tamanho, em bytes, do cookie de OTP criptografado.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Somente gravação<br/> | A senha que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Leitura/gravação<br/> | Indica se o recurso de senha de uso único (OTP) do gateway de área de trabalho remota está habilitado.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Leitura/gravação<br/> | O endereço Web do servidor de pré-autenticação.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Leitura/gravação<br/> | O endereço Web do site que fornece suporte técnico para o servidor de gateway de área de trabalho remota.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Leitura/gravação<br/> | O nome de usuário que um usuário fornece para se conectar ao servidor de gateway de área de trabalho remota.<br/>                |



 

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
</dt> </dl>

 

 





