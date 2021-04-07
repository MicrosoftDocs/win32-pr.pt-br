---
title: Associando a Active Directory Domain Services
description: Em Active Directory Domain Services, o ato de associar um objeto programático a um objeto de Active Directory Domain Services específico é conhecido como associação.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Associação a Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, associação a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920192"
---
# <a name="binding-to-active-directory-domain-services"></a>Associando a Active Directory Domain Services

Em Active Directory Domain Services, o ato de associar um objeto programático a um objeto de Active Directory Domain Services específico é conhecido como *Associação*. Quando um objeto programático, como um objeto [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) , é associado a um objeto de diretório específico, o objeto programático é considerado *associado ao* objeto de diretório.

## <a name="binding-functions-and-methods"></a>Funções e métodos de associação

O método de ligação programaticamente a um objeto Active Directory dependerá da tecnologia de programação usada. Para obter mais informações sobre a associação a objetos no Active Directory Domain Services com uma tecnologia de programação específica, consulte os tópicos listados na tabela a seguir.



| Tecnologia de programação                                                                       | Para obter mais informações                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Associação a um objeto ADSI](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [Protocolo Lightweight Directory Access](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Estabelecendo uma sessão LDAP](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Associação a objetos de diretório](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Cadeias de vinculação

Todos os métodos e funções de associação exigem uma cadeia de caracteres de associação. A forma da cadeia de vinculação depende do provedor. Os Active Directory Domain Services têm suporte de dois provedores, LDAP e WinNT.

A partir do Windows 2000, o provedor LDAP é usado para acessar Active Directory Domain Services. A cadeia de caracteres de associação LDAP pode ter um dos seguintes formatos:

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

Nos exemplos acima, "LDAP:" especifica o provedor LDAP. "GC:" usa o provedor LDAP para associar ao serviço de catálogo global para executar consultas rápidas.

" &lt; nome &gt; do host" especifica o servidor a ser associado e é opcional. Se possível, não especifique um servidor. Também é possível associar a um objeto em um domínio diferente. Para fazer isso, passe o nome DNS (sistema de nomeação de domínio) do domínio de destino para " &lt; nome do host &gt; ". Por exemplo, para associar ao contêiner usuários no domínio domain2 de fabrikam.com, a cadeia de caracteres de associação seria "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com".

" &lt; nome &gt; do objeto" representa um objeto específico em Active Directory Domain Services. O nome do objeto pode ser um nome diferenciado ou um GUID de objeto.

Para obter mais informações sobre cadeias de vinculação LDAP, consulte [ADsPath do LDAP](/windows/desktop/ADSI/ldap-adspath).

Para o Windows NT 4,0, o provedor WinNT é usado para acessar dados de diretório, como usuários, grupos de usuários, computadores, serviços e outros objetos de rede no Windows 2000. O provedor WinNT no Windows 2000 e sistemas posteriores tem funcionalidade limitada em comparação com o provedor LDAP. Para obter mais informações sobre cadeias de vinculação de WinNT, consulte o [ADsPath do Winnt](/windows/desktop/ADSI/winnt-adspath).

Um ADsPath de "LDAP://" ou "GC://" pode ser usado para associar à raiz do namespace. Quando associado à raiz do namespace, o objeto namespace fornecido não contém propriedades e contém o objeto de domínio para LDAP e um objeto de contêiner que contém uma réplica parcial de todos os domínios na floresta para GC.

Para obter mais informações sobre associação em Active Directory Domain Services, consulte:

-   [Associação sem servidor e RootDSE](serverless-binding-and-rootdse.md)
-   [Associação ao catálogo global](binding-to-the-global-catalog.md)
-   [Usando objectGUID para associar a um objeto](using-objectguid-to-bind-to-an-object.md)
-   [Associação a objetos Well-Known usando WKGUID](binding-to-well-known-objects-using-wkguid.md)
-   [Associação a um objeto usando um SID](binding-to-an-object-using-a-sid.md)
-   [Habilitando a associação de Rename-Safe com a propriedade otherWellKnownObjects](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [Autenticação](authentication.md)

 

 
