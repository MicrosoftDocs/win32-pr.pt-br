---
title: Interface IMsRdpClientTransportSettings
description: Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota). | Interface IMsRdpClientTransportSettings
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientTransportSettings
- Serviços de Área de Trabalho Remota da interface IMsRdpClientTransportSettings, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd2cbcdaba0a4324c4501339e972f8bb967f64716d1688cef7c3c38bb22b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771446"
---
# <a name="imsrdpclienttransportsettings-interface"></a>Interface IMsRdpClientTransportSettings

Gerencia as configurações de transporte do cliente para o servidor de gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

## <a name="members"></a>Membros

A interface **IMsRdpClientTransportSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientTransportSettings** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientTransportSettings** tem essas propriedades.



| Propriedade                                                                                                          | Tipo de acesso           | Descrição                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [**GatewayCredsSource**](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | Leitura/gravação<br/> | O método de autenticação do servidor de gateway de área de trabalho remota.<br/>     |
| [**GatewayDefaultUsageMethod**](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | Somente leitura<br/>  | O método de uso do gateway RD padrão.<br/>             |
| [**GatewayHostname**](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | Leitura/gravação<br/> | Nome do host do servidor de gateway de área de trabalho remota.<br/>              |
| [**GatewayIsSupported**](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | Somente leitura<br/>  | Indica se há suporte para o Gateway RD.<br/>       |
| [**GatewayProfileUsageMethod**](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | Leitura/gravação<br/> | O método de uso de perfil de gateway de área de trabalho remota.<br/>             |
| [**GatewayUsageMethod**](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | Leitura/gravação<br/> | O método de uso do servidor de gateway de área de trabalho remota.<br/>              |
| [**GatewayUserSelectedCredsSource**](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | Leitura/gravação<br/> | A origem da credencial do gateway de área de trabalho remota especificada pelo usuário.<br/> |



 

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

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

