---
title: Método SetUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy dados
description: Define a propriedade UserGroupNames para a política Área de Trabalho Remota de autorização de recursos (RD \ 160; VIOLA).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Método SetUserGroupNames Serviços de Área de Trabalho Remota
- Método SetUserGroupNames Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota , método SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d4a54f042ebf99ff5a3b1bf16081ce0719578ef7fc2fd272e9ccc07a832822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008566"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método SetUserGroupNames da classe \_ Win32 TSGatewayResourceAuthorizationPolicy

Define a **propriedade UserGroupNames** para a política Área de Trabalho Remota de autorização de recurso (RD VIOLA).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UserGroupNames* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de grupo de usuários. Os nomes são do formato *Domain \\ UserGroupName*. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentários

Se vários nomes de grupo de usuários estão no *parâmetro UserGroupNames* e um dos nomes não pode ser processado, nenhum dos nomes será processado.

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

