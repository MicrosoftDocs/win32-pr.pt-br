---
title: Classe Win32_TSLicenseServer
description: Fornece métodos e propriedades para exibir e configurar o licenciamento de Área de Trabalho Remota (Licenciamento RD) em um servidor de licença Área de Trabalho Remota.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseServer Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseServer classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918727"
---
# <a name="win32_tslicenseserver-class"></a>\_Classe Win32 TSLicenseServer

Fornece métodos e propriedades para exibir e configurar o licenciamento de Área de Trabalho Remota (Licenciamento RD) em um servidor de licença Área de Trabalho Remota.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSLicenseServer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSLicenseServer** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Ativa o Área de Trabalho Remota servidor de licença usando uma ID de servidor de licença de Área de Trabalho Remota que é obtida pelo telefone ou pela Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Ativa a Área de Trabalho Remota servidor de licença automaticamente pela Internet. As propriedades **FirstName**, **LastName**, **Company** e **CountryRegion** não devem estar vazias quando esse método for chamado ou o método falhará.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Adiciona o Área de Trabalho Remota servidor de licença ao grupo Área de Trabalho Remota servidores de licença em um controlador de domínio no mesmo domínio que o servidor de licença.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Altera o escopo de descoberta do servidor de licença Área de Trabalho Remota.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Não há suporte para o método.<br/> **Windows server 2008 R2 e Windows server 2008:** Cria o grupo local computadores Terminal Server no Área de Trabalho Remota servidor de licença.<br/>                                               |
| [**DeactivateServer**](deactivateserver-win32-tslicenseserver.md)                       | Desativa o servidor de licença Área de Trabalho Remota usando um código de confirmação que é recebido pelo telefone.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Desativa o servidor de licença Área de Trabalho Remota pela Internet. As propriedades **FirstName** e **LastName** não devem estar vazias quando esse método for chamado ou o método apresentar falha.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera o status de ativação atual.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera uma Área de Trabalho Remota ID do servidor de licença se o servidor estiver ativado no momento.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera se o servidor de licença Área de Trabalho Remota é membro do grupo de servidores de licença Área de Trabalho Remota em um controlador de domínio em um determinado domínio.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera se o Licenciamento RD está instalado em um controlador de domínio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera se a configuração da política de grupo "impedir atualização de licença" está habilitada no servidor de licença Área de Trabalho Remota.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera se o servidor de licença Área de Trabalho Remota está publicado no Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera se o servidor de licença Área de Trabalho Remota está registrado como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera se a configuração da política de grupo "grupo de segurança do servidor de licenças" está habilitada no servidor de licença Área de Trabalho Remota.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera se um servidor de Host da Sessão RD tem permissão para solicitar Serviços de Área de Trabalho Remota licenças de acesso para cliente (RDS CALs) do servidor de licença Área de Trabalho Remota.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Não há suporte para o método.<br/> **Windows server 2008 R2 e Windows server 2008:** Recupera se o grupo local computadores Terminal Server existe no servidor de licença Área de Trabalho Remota.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera se um servidor de Host da Sessão RD é membro do grupo local de computadores Terminal Server no servidor de licença Área de Trabalho Remota.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Publica o servidor de licença Área de Trabalho Remota no AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Reativa o servidor de licença Área de Trabalho Remota usando uma nova ID de servidor de licença de Área de Trabalho Remota que é obtida pelo telefone ou pela Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Reativa o servidor de licença Área de Trabalho Remota pela Internet. As propriedades **FirstName** e **LastName** não devem estar vazias quando esse método for chamado ou o método apresentar falha.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra o servidor de licença de Área de Trabalho Remota como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Remove o Área de Trabalho Remota servidor de licença do grupo Área de Trabalho Remota servidores de licenças em um controlador de domínio no mesmo domínio que o servidor de licença.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Não há suporte para o método.<br/> **Windows server 2008 R2 e Windows server 2008:** Remove o grupo local computadores Terminal Server do Área de Trabalho Remota servidor de licença.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Cancelar a publicação de um servidor de licença Área de Trabalho Remota do AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Remove o servidor de licença Área de Trabalho Remota como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseServer** tem essas propriedades.

<dl> <dt>

**Endereço**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Endereço do contato para o Licenciamento RD. Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)

</dd> <dt>

**Cidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Cidade do contato para Licenciamento RD. Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)

</dd> <dt>

**Empresa**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Empresa do contato para Licenciamento RD. Essa propriedade é usada (e obrigatória) quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.

</dd> <dt>

**CountryRegion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

País/região do contato para Licenciamento RD. Essa propriedade é usada (e obrigatória) quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Caminho do banco de dados de licenciamento do RDS.

</dd> <dt>

**Email**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Endereço de email do contato para o Licenciamento RD. Essa propriedade é usada quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados. (Essa propriedade é opcional para essas chamadas de método.)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Nome do contato para o Licenciamento RD. Essa propriedade é usada (e obrigatória) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.

</dd> <dt>

**Sobrenome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sobrenome do contato para o Licenciamento RD. Essa propriedade é usada (e obrigatória) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Unidade organizacional do contato para Licenciamento RD. Essa propriedade é usada quando o [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Código postal do contato para o Licenciamento RD. Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ID do produto do servidor de licença de Área de Trabalho Remota.

</dd> <dt>

**ServerRole**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve o escopo de licenciamento para o servidor de licença Área de Trabalho Remota dentro da organização.

<dt>

0
</dt> <dd>

Host da Sessão RD servidores no mesmo grupo de trabalho podem descobrir o servidor de licença.

</dd> <dt>

1
</dt> <dd>

Host da Sessão RD servidores no mesmo domínio podem descobrir o servidor de licença.

</dd> <dt>

2
</dt> <dd>

Host da Sessão RD servidores de vários domínios na mesma floresta podem descobrir o servidor de licença.

</dd> </dl>

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Estado do contato para o Licenciamento RD. Essa propriedade é usada quando o método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o método **ActivateServerAutomatic** .)

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do servidor de licença do Área de Trabalho Remota.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de versão do servidor de licença de Área de Trabalho Remota.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe é uma classe [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e pode ter apenas uma instância. Todos os métodos contidos nessa classe são estáticos.

Você deve ser um membro do grupo Administradores para usar essa classe. Se o chamador não for um membro do grupo Administradores, as propriedades retornadas estarão vazias.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> </dl>

 

