---
title: Interface IMsRdpClientTransportSettings3
description: Define propriedades adicionais para o servidor de gateway de Área de Trabalho Remota (Gateway RD). | Interface IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings3
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings3, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837757"
---
# <a name="imsrdpclienttransportsettings3-interface"></a>Interface IMsRdpClientTransportSettings3

Define propriedades adicionais para o servidor de gateway de Área de Trabalho Remota (Gateway RD).

## <a name="members"></a>Membros

A interface **IMsRdpClientTransportSettings3** herda de [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md). **IMsRdpClientTransportSettings3** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientTransportSettings3** tem essas propriedades.



| Propriedade                                                                                                           | Tipo de acesso           | Descrição                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GatewayAuthCookieServerAddr**](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | Leitura/gravação<br/> | O endereço do servidor para autenticação baseada em cookie.<br/>                                                                                       |
| [**GatewayAuthLoginPage**](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | Leitura/gravação<br/> | O endereço da página da Web de logon a ser usada para autenticar um usuário.<br/>                                                                           |
| [**GatewayCredSourceCookie**](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | Leitura/gravação<br/> | Especifica se a origem da credencial é baseada em cookie.<br/>                                                                                       |
| [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | Leitura/gravação<br/> | O cookie de autenticação criptografado.<br/>                                                                                                      |
| [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | Leitura/gravação<br/> | O tamanho, em caracteres, da propriedade [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7<br/>                                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings3 é definido como 3D5B21AC-748D-41DE-8F30-E15169586BD4<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





