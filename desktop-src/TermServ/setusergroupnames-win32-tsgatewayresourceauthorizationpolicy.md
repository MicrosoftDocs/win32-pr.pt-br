---
title: Método SetUserGroupNames da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Define a propriedade usergroupnames para a política de autorização de recursos de Área de Trabalho Remota (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetUserGroupNames
- Método SetUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método SetUserGroupNames
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
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085759"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método SetUserGroupNames da classe Win32 \_ TSGatewayResourceAuthorizationPolicy

Define a propriedade **Usergroupnames** para o área de trabalho remota RD RAP (política de autorização de recursos).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Usergroupnames* \[ no\]
</dt> <dd>

Lista de nomes de grupos de usuários separados por ponto e vírgula. Os nomes são do formato *domínio \\ userGroupName*. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários nomes de grupos de usuários estiverem no parâmetro *Usergroupnames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.

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

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

