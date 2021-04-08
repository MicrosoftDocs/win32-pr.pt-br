---
title: Classe Win32_TSGatewayResourceAuthorizationPolicy
description: Descreve uma política de autorização de recursos do Área de Trabalho Remota (RD \ 160; RAP). Uma RD \ 160; A RAP é usada para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: 284a868d-7856-4a25-ba7b-b4beba8ffffc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayResourceAuthorizationPolicy classe, descrita
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
ms.openlocfilehash: 0c262cb1ce3351c89dc5d7edf3b0d106116e83b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009290"
---
# <a name="win32_tsgatewayresourceauthorizationpolicy-class"></a>\_Classe Win32 TSGatewayResourceAuthorizationPolicy

Descreve um Área de Trabalho Remota RD RAP (política de autorização de recursos). Uma RD RAP é usada para decidir se um usuário está autorizado a se conectar a um recurso especificado por meio do gateway de Área de Trabalho Remota (gateway de área de trabalho remota).

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

A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem esses métodos.



| Método                                                                                          | Descrição                                                                                                         |
|:------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Adiciona os nomes de grupos de usuários especificados aos grupos de usuários existentes na propriedade **Usergroupnames** .<br/>      |
| [**Criar**](create-win32-tsgatewayresourceauthorizationpolicy.md)                             | Cria uma RD RAP.<br/>                                                                                       |
| [**Apagar**](delete-win32-tsgatewayresourceauthorizationpolicy.md)                             | Exclui a RD RAP atual.<br/>                                                                              |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) | Remove os nomes de grupo de usuários especificados dos grupos de usuários existentes na propriedade **Usergroupnames** .<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md)             | Define a propriedade **Description** para a RD RAP.<br/>                                                        |
| [**Sethabilitado**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md)                     | Habilita ou desabilita a RD RAP definindo a propriedade **Enabled** .<br/>                                      |
| [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md)                           | Define a propriedade **Name** para a RD RAP.<br/>                                                               |
| [**Setportnumbers**](setportnumbers-win32-tsgatewayresourceauthorizationpolicy.md)             | Define a propriedade **portnumbers** para a RD RAP.<br/>                                                        |
| [**Fileresource**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md)         | Define as propriedades **ResourceGroupType** e **ResourceGroupName** .<br/>                                     |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)       | Define a propriedade **Usergroupnames** para a RD RAP.<br/>                                                     |
| [**Cumulativo**](update-win32-tsgatewayresourceauthorizationpolicy.md)                             | Atualiza a RD RAP atual.<br/>                                                                              |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayResourceAuthorizationPolicy** tem essas propriedades.

<dl> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição da RD RAP. Essa propriedade é alterada com o método [**SetDescription**](setdescription-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se esta RD RAP está habilitada. Essa propriedade é alterada com o método [**sethabilitado**](setenabled-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome da RD RAP. Essa propriedade é alterada com o método [**SetName**](setname-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**PortNumbers**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de números de porta separados por ponto e vírgula permitidos para esta política. Para permitir qualquer número de porta, defina " \* ".

</dd> <dt>

**De protocolo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de nomes de protocolo separados por ponto e vírgula que estão habilitados para esta política. Os nomes devem corresponder ao retorno do método [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) da classe [**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

**ResourceGroupName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do grupo de recursos. Essa propriedade é alterada com o método [**fileresource**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> <dt>

**ResourceGroupType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica o tipo do grupo de recursos. Essa propriedade é alterada com o método [**fileresource**](setresourcegroup-win32-tsgatewayresourceauthorizationpolicy.md) .

<dt>

RT
</dt> <dd>

Grupo de recursos.

</dd> <dt>

CG
</dt> <dd>

Grupo de computadores, conforme armazenado em Active Directory Domain Services.

</dd> <dt>

OS
</dt> <dd>

Todos os recursos.

</dd> </dl>

</dd> <dt>

**Usergroupnames**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de nomes de grupos de usuários separados por ponto e vírgula. Se o usuário pertencer a qualquer um desses grupos de usuários, o acesso será permitido. Essa propriedade é alterada com os métodos [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md), [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md)e [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayresourceauthorizationpolicy.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

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

 

