---
title: Método IsLogEventEnabled da classe Win32_TSGatewayServerSettings
description: Indica se o tipo de log de eventos especificado está habilitado.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Método IsLogEventEnabled Serviços de Área de Trabalho Remota
- Método IsLogEventEnabled Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7130578287e313e03caf8b63c2e187f401608ad1cdbd575ae9e6bb6450e1adf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606055"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a>Método IsLogEventEnabled da classe \_ TSGatewayServerSettings do Win32

Indica se o tipo de log de eventos especificado está habilitado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EventName* \[ Em\]
</dt> <dd>

Nome do tipo de log de eventos. Esse valor deve ser recuperado usando o [**método GetLogEventName.**](getlogeventname-win32-tsgatewayserversettings.md)

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

*Habilitado* \[ out\]
</dt> <dd>

Indica se o tipo de log de eventos especificado está habilitado.

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

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> <dt>

[**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

