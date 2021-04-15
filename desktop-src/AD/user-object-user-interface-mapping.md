---
title: Mapeamento de interface do usuário de objeto do usuário
description: As tabelas a seguir identificam as páginas de propriedades fornecidas pelo snap-in Active Directory usuários e computadores.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- AD de mapeamento de interface do usuário de objeto do usuário
- AD de mapeamento de interface do usuário, objeto de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc797be7c53ba7759051016ddd0548c8c7124cd2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453907"
---
# <a name="user-object-user-interface-mapping"></a>Mapeamento de interface do usuário de objeto do usuário

As tabelas a seguir identificam as páginas de propriedades fornecidas pelo snap-in Active Directory usuários e computadores. Cada tabela identifica os elementos da interface do usuário da página de propriedades e o atributo associado a esse elemento da interface do usuário. Como as páginas de propriedades exibidas pelo snap-in Active Directory usuários e computadores podem ser estendidas, não é possível fornecer esses dados para todas as páginas exibidas em uma folha de propriedades.

## <a name="general-property-page"></a>Página de propriedades geral

A tabela a seguir lista os rótulos de interface do usuário da página de propriedades **geral** .



| Rótulo da interface do usuário         | Atributo no Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nome       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Sobrenome        | [**sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniciais         | [**iniciais**](/windows/desktop/ADSchema/a-initials)                                     |
| Nome de exibição     | [**displayName**](/windows/desktop/ADSchema/a-displayname)                               |
| Descrição      | [**ndescrição**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Número de telefone | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefone: outros | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Email           | [**Email-endereços**](/windows/desktop/ADSchema/a-mail)                                 |
| Página da Web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Página da Web: outras  | [**url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Página de propriedades da conta

A tabela a seguir lista os rótulos de interface do usuário da página de propriedades da **conta** .



| Rótulo da interface do usuário                                | Atributo no Active Directory Domain Services                                                   | Comentário                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome do logon próprio                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Esse campo é obtido de tudo no atributo [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) que precede o último caractere ' @ '. O último caractere ' @ ' e tudo depois dele é colocado na caixa de combinação de sufixo.                                                                                                                                                      |
| Nome de logon do usuário (anterior ao Windows 2000)      | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Registrar horas                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Fazer Logon em                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Conta bloqueada                   | [**locktime**](/windows/desktop/ADSchema/a-lockouttime) e [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Se o atributo [**locktime**](/windows/desktop/ADSchema/a-lockouttime) não for zero, o atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) será adicionado ao **locktime** e comparado à data e hora atuais para determinar se a conta está bloqueada.                                                                                                                                |
| O usuário deverá alterar a senha no próximo logon | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| O usuário não pode alterar a senha             | N/D                                                                                             | Esse é o controle alterar senha na ACL.                                                                                                                                                                                                                                                                                                                                         |
| Outras opções de conta                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Os itens restantes em opções de conta alternam bits no bitmask de atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (sinalizadores em um DWORD).                                                                                                                                                                                                                                 |
| A conta expira                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | O controle **conta expirará** exibe a data em que a conta irá expirar no final de. O atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) é armazenado como a data em que a conta expira. Por isso, a data exibida no controle **Account Expires** será exibida como um dia anterior à data contida no atributo **accountExpires** . |



 

## <a name="address-property-page"></a>Página de propriedades de endereço

A tabela a seguir lista os rótulos de interface do usuário da página de propriedades de **endereço** .



| Rótulo da interface do usuário        | Atributo no Active Directory Domain Services                                                 | Comentário                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Street          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Sem comentários.                                               |
| Caixa P. O         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Sem comentários.                                               |
| City            | [**debug**](/windows/desktop/ADSchema/a-l)                                                                         | O nome do atributo **l** é um "l" minúsculo como na localidade. |
| Estado/Província  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Sem comentários.                                               |
| CEP | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Sem comentários.                                               |
| País/Região  | [**c**](/windows/desktop/ADSchema/a-c), [**co**](/windows/desktop/ADSchema/a-co)e [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) | Sem comentários.                                               |



 

## <a name="member-of-property-page"></a>Membro da página de propriedades

A tabela a seguir lista os rótulos de interface de usuário do **membro da página de** Propriedades.



| Rótulo da interface do usuário          | Atributo no Active Directory Domain Services   | Comentário                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro de         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Inclui todos os grupos na lista de interface do usuário, exceto o grupo primário, que é representado no anúncio por meio do atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Definir grupo primário | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) do grupo primário.                                                                                  |



 

## <a name="organization-property-page"></a>Página de propriedades da organização

A tabela a seguir mostra os rótulos de interface do usuário da página de propriedades da **organização** .



| Rótulo da interface do usuário       | Atributo no Active Directory Domain Services | Comentário     |
|----------------|-----------------------------------------------|-------------|
| Título          | [**title**](/windows/desktop/ADSchema/a-title)                 | Sem comentários. |
| Departamento     | [**department**](/windows/desktop/ADSchema/a-department)       | Sem comentários. |
| Empresa        | [**corporativa**](/windows/desktop/ADSchema/a-company)             | Sem comentários. |
| Gerente: nome   | [**Manager**](/windows/desktop/ADSchema/a-manager)             | Sem comentários. |
| Subordinados diretos | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Sem comentários. |



 

## <a name="profile-property-page"></a>Página de propriedades do perfil

A tabela a seguir lista os rótulos de interface do usuário da página de propriedades do **perfil** .



| Rótulo da interface do usuário                | Atributo no Active Directory Domain Services | Comentário                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Caminho do Perfil            | [**profilepath**](/windows/desktop/ADSchema/a-profilepath)     | Sem comentários.                                                                                                             |
| Script de logon            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Sem comentários.                                                                                                             |
| Pasta base: caminho local | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se **caminho local** for selecionado, o caminho local será armazenado no atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) . |
| Pasta base: conectar    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Se a **conexão** estiver selecionada, a unidade mapeada será armazenada no atributo [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) .          |
| Pasta base: para         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se a **conexão** estiver selecionada, o caminho será armazenado no atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) .          |



 

## <a name="telephones-property-page"></a>Página de propriedades de telefones

A tabela a seguir lista os elementos da interface do usuário da página de propriedades de **telefones** e seus atributos de Active Directory correspondentes.



| Rótulo da interface do usuário        | Atributo no Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Página Inicial            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Página inicial: outras     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Pager           | [**pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Pager: outros    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Dispositivos móveis          | [**móveis**](/windows/desktop/ADSchema/a-mobile)                                               |
| Dispositivos móveis: outros   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: outro      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Telefone IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Telefone IP: outro | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Observações           | [**detalhes**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Páginas de propriedades ambiente, sessões, controle remoto e perfil de serviços de terminal

As páginas **ambiente**, **sessões**, **controle remoto** e **perfil de serviços de terminal** são fornecidas para um objeto de usuário oferecer suporte aos serviços de terminal. Os elementos da interface do usuário para essas páginas não correspondem a atributos individuais. Em vez disso, as configurações são armazenadas em dados privados no Active Directory Domain Services. As configurações dos serviços de terminal podem ser acessadas com a interface [**IADsTsUserEx**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) .

 

 