---
title: Escolhendo a tecnologia de pesquisa
description: Este tópico inclui uma lista de tecnologias usadas para pesquisar Active Directory.
ms.assetid: c9e887e3-7de4-4461-bc32-03db71c3e272
ms.tgt_platform: multiple
keywords:
- tecnologias de pesquisa no Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6edba5c87ed438bc0047e0381d7e366cd6cc865
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453952"
---
# <a name="choosing-the-search-technology"></a>Escolhendo a tecnologia de pesquisa

As tecnologias, listadas na tabela a seguir, podem ser usadas para pesquisar no Active Directory Domain Services.



| Tecnologia                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1)<br/> | A classe [DirectorySearcher](/dotnet/api/system.directoryservices.directorysearcher?view=dotnet-plat-ext-3.1) é fornecida pelo namespace [System. DirectoryServices](/dotnet/api/system.directoryservices?view=dotnet-plat-ext-3.1) para permitir a pesquisa em Active Directory Domain Services com .NET Framework. Para obter mais informações, consulte [pesquisando o diretório](/previous-versions/ms180879(v=vs.90)).<br/>                                                                                                                                  |
| [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)<br/>                       | A ADSI fornece a interface [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar um servidor Active Directory, bem como outros serviços de diretório, como NDS, usando LDAP. **IDirectorySearch** é uma interface com que retorna dados de tipo rico, como inteiro, Cadeia de caracteres de octeto, Cadeia de caracteres, descritor de segurança, hora UTC, inteiro grande ou booliano. Para obter mais informações sobre como usar o **IDirectorySearch**, consulte [pesquisando com a interface IDirectorySearch](/windows/desktop/ADSI/searching-with-idirectorysearch).<br/> |
| OLE DB<br/>                                                              | OLE DB é um conjunto de interfaces COM que fornece aos aplicativos acesso uniforme a dados armazenados em diversas fontes de dados, independentemente do local ou tipo. A ADSI também fornece um provedor de OLE DB para ADSI que permite que os aplicativos usem OLE DB para acessar Active Directory Domain Services. O provedor de OLE DB ADSI usa as interfaces [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para enviar consultas para Active Directory Domain Services e coletar os resultados.<br/>                                     |
| ADO e outras tecnologias de acesso a dados baseadas em OLE DB<br/>                 | O provedor de OLE DB ADSI permite que qualquer tecnologia de acesso a dados baseada em OLE DB, como o ADO, pesquise em Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| API LDAP<br/>                                                            | Os controladores de domínio do Windows 2000 são servidores de diretório que são compatíveis com a versão 3 do LDAP. A API LDAP é uma biblioteca de funções de estilo C. Os aplicativos podem usar a API LDAP para pesquisar dentro do Active Directory Domain Services.<br/>                                                                                                                                                                                                                                                                              |



 

Considere o seguinte ao escolher uma tecnologia:

-   Para o Microsoft Visual Basic e o Visual Basic Scripting Edition (VBScript), o ADO é recomendado.
-   Para C/C++, você pode escolher qualquer uma das tecnologias.
-   Se seu aplicativo usa extensivamente a ADSI, pode ser mais simples usar o [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch). Se você usar o [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) para gerenciar objetos no Active Directory Domain Services, use o **IDirectorySearch** para tornar o tratamento das propriedades retornadas da pesquisa mais fácil. **IDirectorySearch** usa as mesmas estruturas [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) que **IDirectoryObject** para representar Propriedades. Além disso, o **IDirectorySearch** é exposto em quase todos os objetos com ADSI. Se você tiver um ponteiro para um objeto COM ADSI, poderá chamar **QueryInterface** para obter um ponteiro **IDirectorySearch** que pode ser usado para executar uma pesquisa iniciando no objeto de diretório representado pelo objeto com ADSI.
-   Se seu aplicativo já usa OLE DB, ADO ou API LDAP, você pode continuar a usar essas tecnologias para pesquisar no Active Directory Domain Services.
-   Se seu aplicativo precisar unir dados de um serviço de Domínio do Active Directory e um banco de dados SQL Server 7, use OLE DB. Usando OLE DB, seu aplicativo pode executar consultas distribuídas que fazem referência a Active Directory Domain Services e tabelas e conjuntos de linhas de um ou mais bancos de dados do Microsoft SQL Server 7.

 

