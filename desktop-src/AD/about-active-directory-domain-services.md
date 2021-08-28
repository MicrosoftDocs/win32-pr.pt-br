---
title: Sobre Active Directory Domain Services
description: Este guia fornece informações essenciais para a integração do Microsoft Active Directory em aplicativos distribuídos projetados para sistemas operacionais que suportam o Active Directory.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, sobre
- Active Directory Domain Services Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5db36807362ba5542fdc6a946905c7ba9f9189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466603"
---
# <a name="about-active-directory-domain-services"></a>Sobre Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Escrevendo aplicativos poderosos que usam Active Directory Domain Services

Este guia fornece informações essenciais para a integração Active Directory Domain Services aplicativos distribuídos projetados para sistemas operacionais que Active Directory Domain Services, incluindo:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Esses tópicos são para desenvolvedores de software. Para problemas de suporte, [consulte Suporte da Microsoft](https://windows.microsoft.com/windows/support#1tc). Para obter informações sobre como administrar o Active Directory, [consulte Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) em TechNet.

 

## <a name="fundamental-directory-features"></a>Recursos fundamentais do diretório

Um serviço de diretório é um serviço fundamental para aplicativos distribuídos. Um serviço de diretório deve fornecer os recursos listados na tabela a seguir.



| Recurso               | Descrição                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Transparência do local | Capaz de encontrar dados de usuário, grupo, serviço em rede ou recurso sem o endereço do objeto           |
| Dados de objetos           | Capaz de armazenar dados de usuário, grupo, organização e serviço em uma árvore hierárquica                    |
| Consulta rica            | Capaz de localizar um objeto consultando propriedades de objeto                                          |
| Alta disponibilidade     | Capaz de localizar uma réplica do diretório em um local eficiente para operações de leitura/gravação |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Recursos avançados do Active Directory Domain Services

Active Directory Domain Services fornece os recursos listados na tabela a seguir.




| Recurso | Descrição | 
|---------|-------------|
| Suporte para padrões de Internet | Active Directory Domain Services implementa seus recursos de acordo com os padrões publicados da Internet, como LDAP e DNS. | 
| Segurança fortemente integrada e flexível | As vantagens incluem:<br /><ul><li>Escolha de pacotes de autenticação. Kerberos, protocolo SSL (SSL) ou uma combinação; por exemplo, estabeleça um canal SSL para criptografia e, em seguida, use Kerberos para autenticação.</li><li>Gerenciamento central de acesso a serviços e recursos usando os usuários e grupos no Active Directory Domain Services.</li><li>Delegação de administração para que os administradores centrais possam delegar tarefas administrativas, como alteração de senha ou criação e exclusão de objetos específicos.</li><li>O servidor do Active Directory usa os mesmos mecanismos de controle de acesso usados em sistemas de arquivos Windows sistemas operacionais. Portanto, as mesmas ferramentas que gerenciam o controle de acesso em um sistema de arquivos funcionam para Active Directory Domain Services.</li><li>Infraestrutura abrangente de Chave Pública. O suporte ao Servidor de Certificados da Microsoft e ao Cartão Inteligente é integrado ao Active Directory Domain Services para fornecer logon de cartão inteligente e gerenciamento de certificados.</li></ul> | 
| Facilmente programável | O servidor do Active Directory pode ser acessado e administrado programaticamente usando a API de Interfaces de Serviço do <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory,</a> a API do <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> ou o namespace <a href="/dotnet/api/system.directoryservices">System.DirectoryServices.</a> | 
| Serviços do sistema habilitados para diretório | Seu aplicativo cliente pode ser facilmente implantado em áreas de trabalho distribuídas criando um pacote do instalador Windows e usando o recurso de implantação de aplicativo disponível nos sistemas operacionais Windows aplicativos. | 
| Integração de aplicativos principais | Os principais aplicativos distribuídos, como Exchange, são integrados ao Active Directory Domain Services. Portanto, as empresas podem reduzir o número de serviços de diretório a serem gerenciados. | 
| Esquema rico e extensível | O esquema define quais objetos e propriedades podem ser gravados e lidos de um serviço de diretório. O esquema do Active Directory é rico. A maioria dos objetos e propriedades que um serviço requer está disponível. Caso não seja, um aplicativo distribuído pode estender o esquema para dar suporte aos requisitos do aplicativo. | 




 

Para obter mais informações sobre Active Directory Domain Services, consulte:

-   [Principais conceitos de Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Arquitetura do Active Directory](active-directory-domain-services-architecture.md)
-   [Esquema do Active Directory](active-directory-schema.md)

