---
description: Um armazenamento de política de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos.
ms.assetid: bce85da8-11de-4bc1-b097-d8efdbd28abf
title: Criando um objeto de armazenamento de política de autorização no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 409a22df52d2914cd205700afccfc7a59f19031d924a921b5f2e5101621a895a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782191"
---
# <a name="creating-an-authorization-policy-store-object-in-script"></a>Criando um objeto de armazenamento de política de autorização no script

Um armazenamento de política de autorização contém informações sobre a política de segurança de um aplicativo ou grupo de aplicativos. As informações incluem aplicativos, operações, tarefas, usuários e grupos de usuários associados à loja. Quando um aplicativo que usa o Gerenciador de Autorização é inicializado, ele carrega essas informações do armazenamento. O armazenamento de política de autorização deve estar localizado em um sistema confiável porque os administradores nesse sistema têm um alto grau de acesso ao armazenamento.

O Gerenciador de Autorização dá suporte ao armazenamento de política de autorização no serviço de diretório do Active Directory ou em um arquivo XML, conforme mostrado nos exemplos a seguir. Na API do Gerenciador de Autorização, um repositório de políticas de autorização é representado por um [**objeto AzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) Os exemplos mostram como criar um objeto **AzAuthorizationStore** para um repositório do Active Directory e um repositório XML.

-   [Criando um armazenamento do Active Directory](#creating-an-active-directory-store)
-   [Criando um SQL Server Store](#creating-a-sql-server-store)
-   [Criando um armazenamento XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Criando um armazenamento do Active Directory

Para usar o Active Directory para armazenar a política de autorização, o domínio deve estar no nível **funcional Windows Server 2003.** O armazenamento de política de autorização não pode estar localizado em um **contexto de nomen entre** domínios (também chamado de partição de aplicativo). É recomendável que o armazenamento  seja localizado no contêiner Dados do Programa em uma nova unidade organizacional criada especificamente para o armazenamento de política de autorização. Também é recomendável que o armazenamento seja localizado dentro da mesma rede local que os servidores de aplicativos que executem aplicativos que usam o armazenamento.

O exemplo a seguir mostra como criar um [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização no Active Directory. O exemplo supõe que haja uma unidade organizacional existente do Active Directory chamada Dados do Programa em um domínio chamado authmanager.com.


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



## <a name="creating-a-sql-server-store"></a>Criando um SQL Server Store

O Gerenciador de Autorização dá suporte à criação de Microsoft SQL Server de política de autorização baseada em banco de dados. Para criar um SQL Server de autorização baseado em SQL Server, use uma URL que comece com o prefixo **MSSQL://**. A URL deve conter uma cadeia SQL de conexão válida, um nome de banco de dados e o nome do repositório de política de autorização: **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

Se a instância do SQL Server não contém o banco de dados do Gerenciador de Autorização especificado, o Gerenciador de Autorização cria um novo banco de dados com esse nome.

> [!Note]  
> As conexões com um SQL Server não são criptografadas, a menos que você tenha definido explicitamente SQL criptografia para a conexão ou configurar a criptografia do tráfego de rede que usa a IPsec (Segurança de Protocolo da Internet).

 

O exemplo a seguir mostra como criar um [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de políticas de autorização em um banco de SQL Server dados.


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



## <a name="creating-an-xml-store"></a>Criando um armazenamento XML

O Gerenciador de Autorização dá suporte à criação de um armazenamento de política de autorização no formato XML. O armazenamento XML pode estar localizado no mesmo computador em que o aplicativo é executado ou pode ser armazenado remotamente. Não há suporte para a edição do arquivo XML diretamente. Use o snap-in do MMC do Gerenciador de Autorização ou a API do Gerenciador de Autorização para editar o armazenamento de políticas.

O Gerenciador de Autorização não dá suporte à delegação de administração de um armazenamento de políticas XML. Para obter informações sobre delegação, [consulte Delegando a definição de permissões no script](delegating-the-defining-of-permissions-in-script.md).

O exemplo a seguir mostra como criar um [**objeto AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) que representa um repositório de política de autorização em um arquivo XML.


```VB
'  Create the store object.
Dim authStore
Set authStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the store object.
authStore.Initialize 1, "msxml://C:\MyStore.xml"

'  Save information to the store.
authStore.Submit
```



 

 



