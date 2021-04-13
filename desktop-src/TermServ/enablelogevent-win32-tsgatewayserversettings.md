---
title: Método EnableLogEvent da classe Win32_TSGatewayServerSettings
description: Habilita ou desabilita o registro em log do tipo de evento especificado.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método EnableLogEvent
- Método EnableLogEvent Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método EnableLogEvent
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
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456013"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableLogEvent da classe Win32 \_ TSGatewayServerSettings

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

*Eventoname* \[ no\]
</dt> <dd>

O nome do evento. Esse valor deve ser recuperado usando o método [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .

<dt>

LogChannelDisconnect
</dt> <dd>

Usuário desconectado do recurso com êxito.

</dd> <dt>

LogFailedChannelConnect
</dt> <dd>

O usuário não pôde se conectar ao recurso.

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

Usuário conectado com êxito ao recurso.

</dd> <dt>

LogSuccessfulNetworkAccessCheck
</dt> <dd>

O usuário passou com êxito na autorização de conexão.

</dd> <dt>

LogSuccessfulResourceAccessCheck
</dt> <dd>

Usuário aprovado com êxito na autorização de recursos.

</dd> </dl> </dd> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Especifica se o evento deve ser habilitado ou desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

