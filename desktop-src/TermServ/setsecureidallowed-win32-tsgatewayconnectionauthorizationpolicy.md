---
title: Método SetSecureIdAllowed da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Este método está reservado para uso futuro.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Método SetSecureIdAllowed Serviços de Área de Trabalho Remota
- Método SetSecureIdAllowed Serviços de Área de Trabalho Remota , Win32_TSGatewayConnectionAuthorizationPolicy classe
- Win32_TSGatewayConnectionAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99039cd541ad8ab1746ace55de13f35722ea1ba7ccf52fd1a3de93e39e56798
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865106"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetSecureIdAllowed da classe \_ Win32 TSGatewayConnectionAuthorizationPolicy

Este método está reservado para uso futuro.

Define a **propriedade SecureIdAllowed,** que é reservada para uso futuro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Permitido* \[ Em\]
</dt> <dd>

Novo **valor SecureIdAllowed.**

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

 

