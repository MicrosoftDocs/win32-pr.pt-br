---
title: Sobre Active Directory Domain Services
description: Este guia fornece informações essenciais para integrar o Microsoft Active Directory em aplicativos distribuídos projetados para sistemas operacionais que dão suporte a Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, sobre
- Active Directory Domain Services Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007592"
---
# <a name="about-active-directory-domain-services"></a>Sobre Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Escrevendo aplicativos poderosos que usam Active Directory Domain Services

Este guia fornece informações essenciais para a integração de Active Directory Domain Services em aplicativos distribuídos projetados para sistemas operacionais que dão suporte a Active Directory Domain Services, incluindo:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Esses tópicos são para desenvolvedores de software. Para problemas de suporte, consulte [suporte da Microsoft](https://windows.microsoft.com/windows/support#1tc). Para obter informações sobre como administrar Active Directory, consulte [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) no TechNet.

 

## <a name="fundamental-directory-features"></a>Recursos de diretório fundamental

Um serviço de diretório é um serviço fundamental para aplicativos distribuídos. Um serviço de diretório deve fornecer os recursos listados na tabela a seguir.



| Recurso               | Descrição                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Transparência da localização | Capaz de encontrar dados de usuário, grupo, serviço de rede ou recurso, sem o endereço do objeto           |
| Dados de objetos           | Capaz de armazenar dados de usuário, grupo, organização e serviço em uma árvore hierárquica                    |
| Consulta avançada            | Capaz de localizar um objeto consultando as propriedades do objeto                                          |
| Alta disponibilidade     | Capaz de localizar uma réplica do diretório em um local que seja eficiente para operações de leitura/gravação |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Recursos avançados do Active Directory Domain Services

Active Directory Domain Services fornece os recursos listados na tabela a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Recurso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Suporte para padrões da Internet</td>
<td>Active Directory Domain Services implementa seus recursos de acordo com os padrões de Internet publicados, como LDAP e DNS.</td>
</tr>
<tr class="even">
<td>Segurança totalmente integrada e flexível</td>
<td>As vantagens incluem:<br/>
<ul>
<li>Opção de pacotes de autenticação. Kerberos, protocolo SSL (SSL) ou uma combinação; por exemplo, estabeleça um canal SSL para criptografia e, em seguida, use o Kerberos para autenticação.</li>
<li>Gerenciamento central de acesso de serviço e de recursos usando os usuários e grupos no Active Directory Domain Services.</li>
<li>Delegação de administração para que os administradores centrais possam delegar tarefas administrativas, como alteração de senha ou criação e exclusão de objetos específicos.</li>
<li>O servidor de Active Directory usa os mesmos mecanismos de controle de acesso usados em sistemas de arquivos nos sistemas operacionais Windows. Portanto, as mesmas ferramentas que gerenciam o controle de acesso em um sistema de arquivos funcionam para Active Directory Domain Services.</li>
<li>Infraestrutura de chave pública abrangente. O suporte ao servidor de certificado da Microsoft e ao cartão inteligente são integrados com o Active Directory Domain Services para fornecer logon de cartão inteligente e gerenciamento de certificados.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Programável facilmente</td>
<td>O servidor de Active Directory pode ser acessado e administrado por meio de programação usando a API de <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">interfaces de serviço do Active Directory</a> , a API do protocolo de acesso ao <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">diretório leve</a> ou o namespace <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> .</td>
</tr>
<tr class="even">
<td>Serviços do sistema habilitados para diretório</td>
<td>Seu aplicativo cliente pode ser facilmente implantado em áreas de trabalho distribuídas criando um pacote de Windows Installer e usando o recurso de implantação de aplicativo disponível nos sistemas operacionais Windows.</td>
</tr>
<tr class="odd">
<td>Integração de aplicativos-chave</td>
<td>Os principais aplicativos distribuídos, como o Exchange, são integrados com o Active Directory Domain Services. Portanto, as empresas podem reduzir o número de serviços de diretório a serem gerenciados.</td>
</tr>
<tr class="even">
<td>Esquema rico e extensível</td>
<td>O esquema define quais objetos e propriedades podem ser gravados e lidos a partir de um serviço de diretório. O esquema de Active Directory é avançado. A maioria dos objetos e propriedades que um serviço requer estão disponíveis. Caso contrário, um aplicativo distribuído pode estender o esquema para dar suporte aos requisitos do aplicativo.</td>
</tr>
</tbody>
</table>



 

Para obter mais informações sobre Active Directory Domain Services, consulte:

-   [Conceitos principais do Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Arquitetura de Active Directory](active-directory-domain-services-architecture.md)
-   [Esquema do Active Directory](active-directory-schema.md)

