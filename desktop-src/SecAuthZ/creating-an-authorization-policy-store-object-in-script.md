---
description: Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Criando um objeto de repositório de política de autorização no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: feb02c80408210b663524e2aa914852a853e80ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827454"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Criando um objeto de repositório de política de autorização no script

Um repositório de diretivas de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem os aplicativos, as operações, as tarefas, os usuários e os grupos de usuários associados à loja. Quando um aplicativo que usa o Gerenciador de autorização é inicializado, ele carrega essas informações da loja. O repositório de política de autorização deve estar localizado em um sistema confiável, pois os administradores nesse sistema têm um alto grau de acesso à loja.

O Gerenciador de autorização dá suporte ao armazenamento da política de autorização no serviço de diretório Active Directory ou em um arquivo XML, conforme mostrado nos exemplos a seguir. Na API do Gerenciador de autorização, um repositório de política de autorização é representado por um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Os exemplos mostram como criar um objeto **AzAuthorizationStore** para um repositório de Active Directory e um repositório XML.

-   [Criando um repositório de Active Directory](#creating-an-active-directory-store)
-   [Criando um repositório de SQL Server](#creating-a-sql-server-store)
-   [Criando um repositório XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Criando um repositório de Active Directory

Para usar Active Directory para armazenar a política de autorização, o domínio deve estar no nível funcional de domínio do **Windows Server 2003** . O repositório de diretivas de autorização não pode estar localizado em um **contexto de nomenclatura que não seja de domínio** (também chamado de partição de aplicativo). É recomendável que o repositório esteja localizado no contêiner de **dados do programa** em uma nova unidade organizacional criada especificamente para o repositório de políticas de autorização. Também é recomendável que o repositório esteja localizado na mesma rede de área local que os servidores de aplicativos que executam aplicativos que usam o repositório.

O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização no Active Directory. O exemplo supõe que haja uma Active Directory unidade organizacional denominada dados de programa em um domínio chamado authmanager.com.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _
    "msldap://CN=MyStore, CN=Program Data,DC=authmanager,DC=com"

'  Save the information to the store.
authStore.Submit
```



## <a name="creating-a-sql-server-store"></a>Criando um repositório de SQL Server

O Gerenciador de autorização dá suporte à criação de um repositório de política de autorização baseado em Microsoft SQL Server. Para criar um repositório de autorização baseado em SQL Server, use uma URL que comece com o prefixo **MSSQL://**. A URL deve conter uma cadeia de conexão SQL válida, um nome de banco de dados e o nome do repositório de política de autorização: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Se a instância do SQL Server não contiver o banco de dados do Gerenciador de autorização especificado, o Gerenciador de autorização criará um novo banco de dados com esse nome.

> [!Note]  
> As conexões com um repositório de SQL Server não são criptografadas, a menos que você configure explicitamente a criptografia do SQL para a conexão ou configure a criptografia do tráfego de rede que usa o IPsec (Internet Protocol Security).

 

O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um banco de dados SQL Server.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, _ 
  "MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore"

'  Save information to the store.
authStore.Submit
```



## <a name="creating-an-xml-store"></a>Criando um repositório XML

O Gerenciador de autorização dá suporte à criação de um repositório de política de autorização no formato XML. O repositório XML pode estar localizado no mesmo computador em que o aplicativo é executado, ou pode ser armazenado remotamente. Não há suporte para editar o arquivo XML diretamente. Use o snap-in do MMC do Gerenciador de autorização ou a API do Gerenciador de autorização para editar o repositório de políticas.

O Gerenciador de autorização não dá suporte à delegação de administração de um repositório de políticas XML. Para obter informações sobre delegação, consulte [delegando a definição de permissões no script](delegating-the-defining-of-permissions-in-script.md).

O exemplo a seguir mostra como criar um objeto [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um arquivo XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



