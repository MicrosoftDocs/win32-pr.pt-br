---
title: Método DisablePlugAndPlayDevices da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Define a propriedade PlugAndPlayDevicesDisabled.
ms.assetid: 0cfe9fea-da93-47fa-a9ea-868c78890a53
ms.tgt_platform: multiple
keywords:
- Método DisablePlugAndPlayDevices Serviços de Área de Trabalho Remota
- O método DisablePlugAndPlayDevices Serviços de Área de Trabalho Remota classe Win32_TSGatewayConnectionAuthorizationPolicy ,
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método DisablePlugAndPlayDevices
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePlugAndPlayDevices
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84bbd9c6f44c120d5a47e74219ed071a6e405e70ab0a46b54f707671ff5b2e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609432"
---
# <a name="disableplugandplaydevices-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisablePlugAndPlayDevices da classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Define a **propriedade PlugAndPlayDevicesDisabled.** Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **PlugAndPlayDevicesDisabled** controlará o redirecionamento de dispositivos Plug and Play para sessões estabelecidas por meio do servidor do Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisablePlugAndPlayDevices(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desabilitado* \[ Em\]
</dt> <dd>

Novo valor para a **propriedade PlugAndPlayDevicesDisabled.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

