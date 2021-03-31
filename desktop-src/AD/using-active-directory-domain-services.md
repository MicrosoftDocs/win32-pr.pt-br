---
title: Usar o Active Directory Domain Services
description: Esta seção fornece diretrizes para a gravação de aplicativos que usam ou publicam dados em um serviço de diretório Active Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, usando
- Active Directory Domain Services Active Directory, usando
- Exemplos de Active Directory Active Directory
- Exemplos de Active Directory Domain Services Active Directory
- exemplos Active Directory
- Active Directory Active Directory, exemplos consulte Active Directory Domain Services exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642911"
---
# <a name="using-active-directory-domain-services"></a>Usar o Active Directory Domain Services

Esta seção fornece diretrizes para a gravação de aplicativos que usam ou publicam dados em um serviço de diretório Active Directory.

> [!Note]  
> A documentação a seguir destina-se a programadores de computadores. Se você estiver tentando resolver um erro de impressão Active Directory Home, consulte a [seguinte sugestão](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) nas páginas da Comunidade da Microsoft; Se isso não ajudar, tente essas recomendações no [TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Active Directory Domain Services estão em conformidade com o Lightweight Directory Access Protocol 3,0, que é definido pela RFC 2251 e por outras RFCs. Qualquer um dos seguintes conjuntos de API pode ser usado para acessar Active Directory Domain Services. Cada conjunto de API tem vantagens e desvantagens que dependem da linguagem de programação, do ambiente de programação e do método pretendido de execução. A maioria dos exemplos neste guia usa ADSI, que é compatível com linguagens como C e C++, bem como linguagens em conformidade com a automação, como Microsoft Visual Basic e Visual Basic Scripting Edition.

Para obter mais informações sobre tecnologias de Active Directory Domain Services específicas, consulte:

-   [Protocolo Lightweight Directory Access](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Active Directory Service Interfaces](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

Esta seção aborda os seguintes tópicos:

-   [Associando a Active Directory Domain Services](binding-to-active-directory-domain-services.md)
-   [Pesquisando no Active Directory Domain Services](searching-in-active-directory-domain-services.md)
-   [Criando e excluindo objetos no Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Movendo objetos](moving-objects.md)
-   [Lendo e gravando atributos de objetos no Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Estendendo o esquema](extending-the-schema.md)
-   [Estendendo a interface do usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md)
-   [Gerenciando usuários](managing-users.md)
-   [Gerenciando grupos](managing-groups.md)
-   [Controlando alterações](tracking-changes.md)
-   [Publicação de serviço](service-publication.md)
-   [Contas de logon de serviço](service-logon-accounts.md)
-   [Autenticação mútua usando Kerberos](mutual-authentication-using-kerberos.md)
-   [Fazendo backup e restaurando Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Armazenando Dados Dinâmicos](storing-dynamic-data.md)
-   [Partições de diretório de aplicativos](application-directory-partitions.md)
-   [Detectando o modo de operação de um domínio](detecting-the-operation-mode-of-a-domain.md)

 

 