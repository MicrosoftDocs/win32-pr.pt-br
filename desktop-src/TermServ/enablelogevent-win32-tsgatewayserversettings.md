---
title: Método EnableLogEvent da classe Win32_TSGatewayServerSettings
description: Habilita ou desabilita o registro em log do tipo de evento especificado.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Método EnableLogEvent Serviços de Área de Trabalho Remota
- Método EnableLogEvent Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd70902649f6fadc66308ad35ce165a6d2fdb4654b73e056c3bc38f1850b3e07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871716"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableLogEvent da classe \_ Win32 TSGatewayServerSettings

Habilita ou desabilita o registro em log do tipo de evento especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EventName* \[ Em\]
</dt> <dd>

O nome do evento. Esse valor deve ser recuperado usando o [**método GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

<dt>

LogChannelDisconnect
</dt> <dd>

O usuário foi desconectado com êxito do recurso.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

O usuário não conseguiu se conectar ao recurso.

</dd> <dt>

LogFailureNetworkAccessCheck
</dt> <dd>

Falha na autorização de conexão do usuário.

</dd> <dt>

LogFailureResourceAccessCheck
</dt> <dd>

Falha na autorização de recursos do usuário.

</dd> <dt>

LogSuccessChannelConnect
</dt> <dd>

O usuário se conectou com êxito ao recurso.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

O usuário passou com êxito a autorização de conexão.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

O usuário passou com êxito a autorização de recursos.

</dd> </dl> </dd> <dt>

*Habilitado* \[ Em\]
</dt> <dd>

Especifica se o evento deve ser habilitado ou desabilitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

