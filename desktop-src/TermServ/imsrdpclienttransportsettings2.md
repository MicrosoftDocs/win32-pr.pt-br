---
title: Interface IMsRdpClientTransportSettings2
description: Gerencia as configurações de transporte do cliente para o servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD). | Interface IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- Interface IMsRdpClientTransportSettings2 Serviços de Área de Trabalho Remota
- Interface IMsRdpClientTransportSettings2 Serviços de Área de Trabalho Remota , descrita
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
ms.openlocfilehash: 479fdceee0a1fc168725ef9b5acccb471e1b32b8c13a0e0ff6b12096f14ff0ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000946"
---
# <a name="imsrdpclienttransportsettings2-interface"></a>Interface IMsRdpClientTransportSettings2

Gerencia as configurações de transporte do cliente para o servidor Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="members"></a>Membros

A interface **IMsRdpClientTransportSettings2** herda de [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md). **IMsRdpClientTransportSettings2** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientTransportSettings2** tem essas propriedades.



| Propriedade                                                                                                    | Tipo de acesso           | Descrição                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [**GatewayCredSharing**](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | Leitura/gravação<br/> | Indica se o recurso de login único para o Gateway de RD está habilitado.<br/>                |
| [**GatewayDomain**](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | Leitura/gravação<br/> | O nome de domínio que um usuário fornece para se conectar ao servidor de Gateway de Área de Trabalho Remoto.<br/>              |
| [**GatewayEncryptedOtpCookie**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | Leitura/gravação<br/> | O cookie OTP criptografado.<br/>                                                              |
| [**GatewayEncryptedOtpCookieSize**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | Leitura/gravação<br/> | O tamanho, em bytes, do cookie OTP criptografado.<br/>                                       |
| [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | Somente gravação<br/> | A senha que um usuário fornece para se conectar ao servidor de Gateway de RD.<br/>                 |
| [**GatewayPreAuthRequirement**](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | Leitura/gravação<br/> | Indica se o recurso de senha única (OTP) do Gateway de RD está habilitado.<br/>           |
| [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | Leitura/gravação<br/> | O endereço Web do servidor de pré-autenticação.<br/>                                      |
| [**GatewaySupportUrl**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | Leitura/gravação<br/> | O endereço Web do site que fornece suporte técnico para o servidor de Gateway de Área de Trabalho Remoto.<br/> |
| [**GatewayUsername**](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | Leitura/gravação<br/> | O nome de usuário que um usuário fornece para se conectar ao servidor de Gateway de RD.<br/>                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista com SP1<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 é definido como 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





