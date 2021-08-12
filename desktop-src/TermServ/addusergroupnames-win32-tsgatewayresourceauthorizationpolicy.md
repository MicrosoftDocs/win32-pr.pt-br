---
title: Método AddUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Adiciona a lista de nomes de grupo de usuários separados por ponto e vírgula especificado aos grupos de usuários existentes na propriedade UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Método AddUserGroupNames Serviços de Área de Trabalho Remota
- Método AddUserGroupNames Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be87eb72790d5852861fe0066bc32e319f0a74ba00af3d0ea38dc0ebcbee9850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610170"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método AddUserGroupNames da classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Adiciona a lista especificada separada por ponto e vírgula de nomes de grupo de usuários aos grupos de usuários existentes na **propriedade UserGroupNames.**

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserGroupNames* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de grupo de usuários a adicionar à **propriedade UserGroupNames.** Os nomes de grupo de usuários devem estar no formato *Domain \\ UserGroupName*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários nomes de grupo de usuários estão no *parâmetro UserGroupNames* e um dos nomes não pode ser processado, nenhum dos nomes será processado.

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

