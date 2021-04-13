---
title: Método AddUserGroupNames da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Adiciona os nomes de grupos de usuários especificados à propriedade usergroupnames.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddUserGroupNames
- Método AddUserGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369395"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método AddUserGroupNames da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Adiciona os nomes de grupos de usuários especificados à propriedade **Usergroupnames** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Usergroupnames* \[ no\]
</dt> <dd>

Lista separada por ponto-e-vírgula de nomes de grupos de usuários a serem adicionados à propriedade **Usergroupnames** . Os nomes de grupos de usuários devem ter o formato *domínio \\ userGroupName*.

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

