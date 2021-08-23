---
title: Método DisableSerialPorts da classe Win32_TSGatewayConnectionAuthorizationPolicy dados
description: Define a propriedade SerialPortsDisabled.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Método DisableSerialPorts Serviços de Área de Trabalho Remota
- Método DisableSerialPorts Serviços de Área de Trabalho Remota , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método DisableSerialPorts
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff70f3e387a21097500856d7a3f63ff00b7a0c3cf68ad2c7d3e5cd97b079dd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681211"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método DisableSerialPorts da classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Define a **propriedade SerialPortsDisabled.** Se a propriedade **DeviceRedirectionType** tiver um valor de "2", a propriedade **SerialPortsDisabled** controlará o redirecionamento das portas seriais para sessões estabelecidas por meio do servidor do Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Desabilitado* \[ Em\]
</dt> <dd>

Novo valor para a **propriedade SerialPortsDisabled.**

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

