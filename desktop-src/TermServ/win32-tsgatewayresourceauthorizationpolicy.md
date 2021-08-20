---
title: Win32_TSGatewayResourceAuthorizationPolicy classe
description: Descreve uma política de Área de Trabalho Remota de autorização de recursos (RD \ 160; VIOLA). Um RD \ 160; O VIOLA é usado para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway Área de Trabalho Remota (Gateway de RD).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota
- Win32_TSGatewayResourceAuthorizationPolicy classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy.Name
- Win32_TSGatewayResourceAuthorizationPolicy.Description
- Win32_TSGatewayResourceAuthorizationPolicy.Enabled
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupType
- Win32_TSGatewayResourceAuthorizationPolicy.ResourceGroupName
- Win32_TSGatewayResourceAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayResourceAuthorizationPolicy.ProtocolNames
- Win32_TSGatewayResourceAuthorizationPolicy.PortNumbers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9748ddc4feccd504d823025ea70877004417717d625c904ccae4445f05e6eb03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999816"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>Classe Win32 \_ TSGatewayResourceAuthorizationPolicy

Descreve uma política de Área de Trabalho Remota de autorização de recurso (RD VIOLA). Um RD VIOLA é usado para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do Gateway de Área de Trabalho Área de Trabalho Remota (Gateway de Área de Trabalho).

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceAuthorizationPolicy
{
  string  Name;
  string  Description;
  boolean Enabled;
  string  ResourceGroupType;
  string  ResourceGroupName;
  string  UserGroupNames;
  string  ProtocolNames;
  string  PortNumbers;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSGatewayResourceAuthorizationPolicy** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TSGatewayResourceAuthorizationPolicy** tem esses métodos.



| Método                                                                                          | Descrição                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Adiciona os nomes de grupo de usuários especificados aos grupos de usuários existentes na **propriedade UserGroupNames.**<br/>      |
| [**Criar**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Cria um RD VIOLA.<br/>                                                                                       |
| [**Excluir**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Exclui o RD VIOLA atual.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Remove os nomes de grupo de usuários especificados dos grupos de usuários existentes na **propriedade UserGroupNames.**<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Define a **propriedade Description** para o RD VIOLA.<br/>                                                        |
| [**Setenabled**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Habilita ou desabilita o RD VIOLA definindo **a propriedade** Habilitado.<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Define a **propriedade Name** para o RD VIOLA.<br/>                                                               |
| [**SetPortNumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Define a **propriedade PortNumbers** para o RD VIOLA.<br/>                                                        |
| [**SetResourceGroup**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Define as **propriedades ResourceGroupType** **e ResourceGroupName.**<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Define a **propriedade UserGroupNames** para o RD VIOLA.<br/>                                                     |
| [**Atualizar**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Atualiza o RD VIOLA atual.<br/>                                                                              |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSGatewayResourceAuthorizationPolicy** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do RD VIOLA. Essa propriedade é alterada com o [**método SetDescription.**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Habilitada**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se esse RD VIOLA está habilitado. Essa propriedade é alterada com o [**método SetEnabled.**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do RD VIOLA. Essa propriedade é alterada com o [**método SetName.**](setname-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de números de porta separados por ponto e vírgula que são permitidos para essa política. Para permitir qualquer número de porta, de definir " \* ".

</dd> <dt>

**ProtocolNames**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de nomes de protocolo separados por ponto e vírgula que estão habilitados para essa política. Os nomes devem corresponder ao retorno [**do método GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**\_ Win32 TSGatewayServerSettings.**](win32-tsgatewayserversettings.md)

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do grupo de recursos. Essa propriedade é alterada com o [**método SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o tipo do grupo de recursos. Essa propriedade é alterada com o [**método SetResourceGroup.**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)

<dt>

"RG"
</dt> <dd>

Grupo de recursos.

</dd> <dt>

"CG"
</dt> <dd>

Grupo de computadores, conforme armazenado Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Todos os recursos.

</dd> </dl>

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista separada por ponto e vírgula de nomes de grupo de usuários. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido. Essa propriedade é alterada com os métodos [**SetUserGroupNames,**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames.**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

