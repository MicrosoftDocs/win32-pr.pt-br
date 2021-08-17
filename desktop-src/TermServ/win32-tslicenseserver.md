---
title: Win32_TSLicenseServer classe
description: Fornece métodos e propriedades para exibir e configurar o Área de Trabalho Remota (Licenciamento de RD) em um Área de Trabalho Remota de licença.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: 0f7c73c1d1a48bbc76b4988afca8a07fd9ce505d0633c74f67306901259d9f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126506"
---
# <a name="win32_tslicenseserver-class"></a>Classe Win32 \_ TSLicenseServer

Fornece métodos e propriedades para exibir e configurar o Área de Trabalho Remota (Licenciamento de RD) em um Área de Trabalho Remota de licença.

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

A **classe Win32 \_ TSLicenseServer** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Win32 TSLicenseServer** tem esses métodos.



| Método                                                                                   | Descrição                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateServer**](activateserver-win32-tslicenseserver.md)                           | Ativa o servidor Área de Trabalho Remota licença usando uma ID do Área de Trabalho Remota de licença que é obtida por telefone ou Internet.<br/>                                                                                           |
| [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md)         | Ativa o servidor Área de Trabalho Remota de licença automaticamente pela Internet. As **propriedades FirstName**, **LastName**, **Company** e **CountryRegion** não devem estar vazias quando esse método é chamado ou o método falhará.<br/> |
| [**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)                       | Adiciona o Área de Trabalho Remota de licença ao grupo Área de Trabalho Remota servidores de licença em um controlador de domínio no mesmo domínio que o servidor de licença.<br/>                                                                                |
| [**ChangeRole**](changerole-win32-tslicenseserver.md)                                   | Altera o escopo de descoberta do servidor Área de Trabalho Remota licença.<br/>                                                                                                                                                                  |
| [**CreateTSCGroup**](createtscgroup-win32-tslicenseserver.md)                           | Não há suporte para o método.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Cria o grupo local Computadores do Servidor de Terminal Área de Trabalho Remota servidor de licença.<br/>                                               |
| [**DesativarServer**](deactivateserver-win32-tslicenseserver.md)                       | Desativa o servidor Área de Trabalho Remota licença usando um código de confirmação recebido por telefone.<br/>                                                                                                                        |
| [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md)     | Desativa o servidor de Área de Trabalho Remota de licença pela Internet. As **propriedades FirstName** **e LastName** não devem estar vazias quando esse método é chamado ou o método falhará.<br/>                                              |
| [**GetActivationStatus**](getactivationstatus-win32-tslicenseserver.md)                 | Recupera o status de ativação atual.<br/>                                                                                                                                                                                           |
| [**GetLicenseServerId**](getlicenseserverid-win32-tslicenseserver.md)                   | Recupera uma ID Área de Trabalho Remota do servidor de licença se o servidor estiver ativado no momento.<br/>                                                                                                                                                 |
| [**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)                         | Recupera se o servidor Área de Trabalho Remota licença de usuário é membro do grupo Área de Trabalho Remota servidores de licença em um controlador de domínio em um determinado domínio.<br/>                                                                              |
| [**IsLSonDC**](islsondc-win32-tslicenseserver.md)                                       | Recupera se o Licenciamento de Área de Trabalho Local está instalado em um controlador de domínio.<br/>                                                                                                                                                                |
| [**IsLSPreventUpgradeGPEnabled**](islspreventupgradegpenabled-win32-tslicenseserver.md) | Recupera se a configuração de política de grupo "impedir a atualização de licença" está habilitada no servidor Área de Trabalho Remota licença.<br/>                                                                                                              |
| [**IsLSPublished**](islspublished-win32-tslicenseserver.md)                             | Recupera se o servidor Área de Trabalho Remota licença de usuário está publicado Active Directory Domain Services (AD DS).<br/>                                                                                                                      |
| [**IsLSRegisteredToSCP**](win32-tslicenseserver-islsregisteredtoscp.md)                 | Recupera se o servidor Área de Trabalho Remota licença está registrado como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                               |
| [**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)                 | Recupera se a configuração de política de grupo "grupo de segurança do servidor de licença" está habilitada no servidor Área de Trabalho Remota licença.<br/>                                                                                                        |
| [**IsSecureAccessAllowed**](issecureaccessallowed-win32-tslicenseserver.md)             | Recupera se um servidor Host da Sessão RD pode solicitar licenças Serviços de Área de Trabalho Remota de acesso do cliente (CALs RDS) do servidor de Área de Trabalho Remota licença.<br/>                                                                |
| [**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)                     | Não há suporte para o método.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Recupera se o grupo local Computadores Do Servidor de Terminal existe no servidor Área de Trabalho Remota licença.<br/>                              |
| [**IsTSinTSCGroup**](istsintscgroup-win32-tslicenseserver.md)                           | Recupera se um servidor Host da Sessão RD é membro do grupo local Computadores Do Servidor terminal no servidor Área de Trabalho Remota licença.<br/>                                                                                         |
| [**PublishLS**](publishls-win32-tslicenseserver.md)                                     | Publica o servidor Área de Trabalho Remota licença do AD DS.<br/>                                                                                                                                                                              |
| [**ReactivateServer**](reactivateserver-win32-tslicenseserver.md)                       | Reativa o servidor Área de Trabalho Remota licença usando uma nova ID do Área de Trabalho Remota de licença que é obtida pelo telefone ou pela Internet.<br/>                                                                                     |
| [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)     | Reativa o servidor de Área de Trabalho Remota de licença pela Internet. As **propriedades FirstName** **e LastName** não devem estar vazias quando esse método é chamado ou o método falhará.<br/>                                              |
| [**RegisterLSToSCP**](win32-tslicenseserver-registerlstoscp.md)                         | Registra o servidor Área de Trabalho Remota licença como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                                                     |
| [**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)             | Remove o servidor Área de Trabalho Remota licença do grupo Área de Trabalho Remota licenças em um controlador de domínio no mesmo domínio que o servidor de licença.<br/>                                                                           |
| [**RemoveTSCGroup**](removetscgroup-win32-tslicenseserver.md)                           | Não há suporte para o método.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Remove o grupo local Computadores Do Servidor de Terminal do servidor Área de Trabalho Remota licença.<br/>                                             |
| [**UnpublishLS**](unpublishls-win32-tslicenseserver.md)                                 | Não publica um servidor Área de Trabalho Remota licença do AD DS.<br/>                                                                                                                                                                            |
| [**UnRegisterLSFromSCP**](win32-tslicenseserver-unregisterlsfromscp.md)                 | Remove o servidor Área de Trabalho Remota licença como um ponto de conexão de serviço no Active Directory Domain Services.<br/>                                                                                                                       |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSLicenseServer** tem essas propriedades.

<dl> <dt>

**Endereço**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Endereço da rua do contato para Licenciamento de RD. Essa propriedade é usada quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o **método ActivateServerAutomatic.)**

</dd> <dt>

**Cidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Cidade do contato para Licenciamento de RD. Essa propriedade é usada quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o **método ActivateServerAutomatic.)**

</dd> <dt>

**Empresa**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Empresa do contato para Licenciamento de RD. Essa propriedade é usada (e necessária) quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.

</dd> <dt>

**Countryregion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

País/região do contato para licenciamento de área de trabalho. Essa propriedade é usada (e necessária) quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado.

</dd> <dt>

**Databasepath**
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

Tipo de acesso: Leitura/gravação
</dt> </dl>

Endereço de email do contato para Licenciamento de RD. Essa propriedade é usada quando os [**métodos ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados. (Essa propriedade é opcional para essas chamadas de método.)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Nome do contato para Licenciamento de RD. Essa propriedade é usada (e necessária) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.

</dd> <dt>

**Sobrenome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Sobrenome do contato para Licenciamento de RD. Essa propriedade é usada (e necessária) quando os métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)ou [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) são chamados.

</dd> <dt>

**OrgUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Unidade organizacional do contato para Licenciamento de RD. Essa propriedade é usada quando [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o **método ActivateServerAutomatic.)**

</dd> <dt>

**PostalCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Código postal do contato para licenciamento de área de trabalho. Essa propriedade é usada quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o **método ActivateServerAutomatic.)**

</dd> <dt>

**ProductId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ID do produto do servidor Área de Trabalho Remota licença.

</dd> <dt>

**Serverrole**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve o escopo de licenciamento para o Área de Trabalho Remota de licenças na organização.

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

Tipo de acesso: Leitura/gravação
</dt> </dl>

Estado do contato para Licenciamento de RD. Essa propriedade é usada quando [**o método ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) é chamado. (Essa propriedade é opcional ao usar o **método ActivateServerAutomatic.)**

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do servidor Área de Trabalho Remota licença.

</dd> <dt>

**VersionNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de versão do servidor Área de Trabalho Remota licença.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe é uma [classe singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) e pode ter apenas uma instância. Todos os métodos contidos nessa classe são estáticos.

Você deve ser um membro do grupo Administradores para usar essa classe. Se o chamador não for membro do grupo Administradores, as propriedades retornadas estarão vazias.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> </dl>

 

