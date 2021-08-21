---
title: Mapeamento de interface do usuário de objeto do usuário
description: As tabelas a seguir identificam as páginas de propriedades fornecidas pelo Usuários e Computadores do Active Directory snap-in.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- AD de mapeamento Interface do Usuário objeto de usuário
- Interface do Usuário mapeamento do AD , objeto de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024494"
---
# <a name="user-object-user-interface-mapping"></a>Mapeamento de interface do usuário de objeto do usuário

As tabelas a seguir identificam as páginas de propriedades fornecidas pelo Usuários e Computadores do Active Directory snap-in. Cada tabela identifica os elementos de interface do usuário da página de propriedades e o atributo associado a esse elemento de interface do usuário. Como as páginas de propriedades exibidas pelo Usuários e Computadores do Active Directory snap-in podem ser estendidas, não é possível fornecer esses dados para todas as páginas exibidas em uma folha de propriedades.

## <a name="general-property-page"></a>Página de propriedades gerais

A tabela a seguir lista os rótulos de interface do usuário **da página de** propriedades Geral.



| Rótulo da interface do usuário         | Atributo em Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nome       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Sobrenome        | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniciais         | [**Iniciais**](/windows/desktop/ADSchema/a-initials)                                     |
| Nome de Exibição     | [**Displayname**](/windows/desktop/ADSchema/a-displayname)                               |
| Descrição      | [**Descrição**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Número de telefone | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Telefone: outros | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Email           | [**Endereços de email**](/windows/desktop/ADSchema/a-mail)                                 |
| Página da Web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Página da Web: Outros  | [**Url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Página de propriedades da conta

A tabela a seguir lista os rótulos de interface do usuário da **página de propriedades** Conta.



| Rótulo da interface do usuário                                | Atributo em Active Directory Domain Services                                                   | Comentário                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome do UserLogon                          | [**Userprincipalname**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Esse campo é retirado de tudo no [**atributo userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) que precede o último caractere '@'. O último caractere '@' e tudo depois que ele é colocado na caixa de combinação do sufixo.                                                                                                                                                      |
| Nome de logon do usuário (pré-Windows 2000)      | [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Registrar horas                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Fazer Logon em                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| Conta bloqueada                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) e [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Se o [**atributo lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) não for zero, o atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) será adicionado a **lockoutTime** e comparado à data e hora atuais para determinar se a conta está bloqueada.                                                                                                                                |
| O usuário deverá alterar a senha no próximo logon | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Sem comentários.                                                                                                                                                                                                                                                                                                                                                                             |
| O usuário não pode alterar a senha             | N/D                                                                                             | Este é o controle Alterar Senha na ACL.                                                                                                                                                                                                                                                                                                                                         |
| Outras opções de conta                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Os itens restantes em Opções de Conta alternam bits no bitmask do atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (sinalizadores em um DWORD).                                                                                                                                                                                                                                 |
| A conta expira                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | O **controle Conta Expira** exibe a data em que a conta expirará no final. O [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) é armazenado como a data em que a conta expira. Por isso, a data exibida  no controle Conta Expira será exibida como um dia antes da data contida no atributo **accountExpires.** |



 

## <a name="address-property-page"></a>Página De propriedades de endereço

A tabela a seguir lista os rótulos de interface do usuário da **página de** propriedades Endereço.



| Rótulo da interface do usuário        | Atributo em Active Directory Domain Services                                                 | Comentário                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Street          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Sem comentários.                                               |
| P.o.box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Sem comentários.                                               |
| City            | [**L**](/windows/desktop/ADSchema/a-l)                                                                         | O **nome** do atributo l é um "L" minúsculo como em Localidade. |
| Estado/Província  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Sem comentários.                                               |
| Cep/Cep | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Sem comentários.                                               |
| País/Região  | [**c,**](/windows/desktop/ADSchema/a-c) [**co**](/windows/desktop/ADSchema/a-co)e [**countryCode**](/windows/desktop/ADSchema/a-countrycode) | Sem comentários.                                               |



 

## <a name="member-of-property-page"></a>Página Membro da Propriedade

A tabela a seguir lista os rótulos de interface do usuário **da página de propriedades** Membro de .



| Rótulo da interface do usuário          | Atributo em Active Directory Domain Services   | Comentário                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Membro de         | [**Memberof**](/windows/desktop/ADSchema/a-memberof)             | Inclui todos os grupos na lista de interface do usuário, exceto o grupo primário, que é representado no AD por meio do [**atributo primaryGroupId.**](/windows/desktop/ADSchema/a-primarygroupid) |
| Definir grupo primário | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) do grupo primário.                                                                                  |



 

## <a name="organization-property-page"></a>Página de propriedades da organização

A tabela a seguir mostra os rótulos de interface do usuário da **página de propriedades** Organização.



| Rótulo da interface do usuário       | Atributo em Active Directory Domain Services | Comentário     |
|----------------|-----------------------------------------------|-------------|
| Título          | [**Título**](/windows/desktop/ADSchema/a-title)                 | Sem comentários. |
| Departamento     | [**Departamento**](/windows/desktop/ADSchema/a-department)       | Sem comentários. |
| Empresa        | [**Empresa**](/windows/desktop/ADSchema/a-company)             | Sem comentários. |
| Manager:Name   | [**manager**](/windows/desktop/ADSchema/a-manager)             | Sem comentários. |
| Relatórios diretos | [**Directreports**](/windows/desktop/ADSchema/a-directreports) | Sem comentários. |



 

## <a name="profile-property-page"></a>Página de propriedades do perfil

A tabela a seguir lista os rótulos de interface do usuário da **página de propriedades** Perfil.



| Rótulo da interface do usuário                | Atributo em Active Directory Domain Services | Comentário                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Caminho do Perfil            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Sem comentários.                                                                                                             |
| Logon Script            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Sem comentários.                                                                                                             |
| Pasta Base: Caminho Local | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se **Caminho local** estiver selecionado, o caminho local será armazenado no atributo [**homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory) |
| Pasta Base: Conexão    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Se **Conexão** estiver selecionada, a unidade mapeada será armazenada no [**atributo homeDrive.**](/windows/desktop/ADSchema/a-homedrive)          |
| Pasta Base: para         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Se **Conexão** estiver selecionado, o caminho será armazenado no [**atributo homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory)          |



 

## <a name="telephones-property-page"></a>Página de propriedades de telefones

A tabela a seguir lista os elementos de interface do usuário da página de propriedades De telefone e seus atributos **correspondentes** do Active Directory.



| Rótulo da interface do usuário        | Atributo em Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Página Inicial            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Home: Outros     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Pager           | [**Pager**](/windows/desktop/ADSchema/a-pager)                                                 |
| Pager: Outros    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Dispositivos móveis          | [**Móvel**](/windows/desktop/ADSchema/a-mobile)                                               |
| Móvel: Outros   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: Outros      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Telefone IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Telefone IP: outros | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Observações           | [**informações**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Páginas de propriedades ambiente, sessões, controle remoto e perfil de serviços de terminal

As **páginas Ambiente,** **Sessões,** **Controle Remoto** e Perfil de Serviços de **Terminal** são fornecidas para um objeto de usuário dar suporte a serviços de terminal. Os elementos da interface do usuário para essas páginas não correspondem a atributos individuais. Em vez disso, as configurações são armazenadas em dados privados em Active Directory Domain Services. As configurações de serviços de terminal podem ser acessadas com a interface [**IADsTsUserEx.**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex)

 

 