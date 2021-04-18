---
title: Consulta Distribuída
description: Como o ADSI é um provedor de OLE DB, ele pode participar da consulta distribuída introduzida no Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- ADSI de consultas, consulta distribuída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "105755903"
---
# <a name="distributed-query"></a>Consulta Distribuída

Como o ADSI é um provedor de OLE DB, ele pode participar da consulta distribuída introduzida no Microsoft SQL Server 7,0. Estes são os possíveis cenários:

-   Unindo objetos de Active Directory com dados de SQL Server.
-   Atualizando dados SQL de objetos Active Directory.
-   Criando junções de três vias ou quatro vias com outros provedores de OLE DB. Por exemplo, servidor de índice, SQL Server e Active Directory.

O provedor de OLE DB dá suporte a dois dialetos de comando, LDAP e SQL, para acessar o serviço de diretório e retornar resultados em um formulário de tabela que pode ser consultado com SQL Server consultas distribuídas.

**Para iniciar o analisador de consultas SQL**

1.  Primeiro, abra o [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) no SQL Server que está vinculado ao serviço de diretório (consulte Criando um servidor vinculado).
2.  Execute o **SQL Query Analyzer** (iniciar \| programas \| Microsoft SQL Server 7,0)
3.  Faça logon no computador SQL Server.
4.  Insira a consulta SQL no painel do editor da janela de consulta.
5.  Execute a consulta pressionando F5.

As seções a seguir fornecem mais detalhes:

-   [Criando um servidor vinculado](#creating-a-linked-server)
-   [Criando um logon SQL Server autenticado](#creating-a-sql-server-authenticated-login)
-   [Consultando o serviço de diretório](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Criando um servidor vinculado

Para configurar uma junção distribuída em um serviço de diretório do Windows 2000 Server, crie um servidor vinculado. Para fazer isso, configure o mapeamento ADSI usando o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) . Este procedimento vincula um nome a um nome de provedor de OLE DB.

No exemplo a seguir, observe que há vários argumentos usados com o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :

-   "ADSI" é o argumento de **servidor** e será o nome desse servidor vinculado.
-   "Active Directory Services 2,5" é o argumento **srvproduct** , que é o nome da fonte de dados OLE DB que você está adicionando como um servidor vinculado.
-   "ADSDSOObject" é o argumento de **\_ nome do provedor** .
-   "adsdatasource" é o argumento de **\_ fonte de dados** , que é o nome da fonte de dados conforme interpretado pelo provedor de OLE DB.

O comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Para logons autenticados pelo Windows, o mapeamento automático é suficiente para acessar o diretório com SQL Server delegação de segurança. Como o mapeamento automático é criado por padrão para servidores vinculados criados por meio do [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), nenhum outro mapeamento de logon é necessário.

Para os logons SQL Server autenticados, você pode configurar logons e senhas adequados para se conectar ao serviço de diretório usando o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

> [!Note]  
> Quando possível, use a Autenticação do Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Criando um logon SQL Server autenticado

Se você preferir usar um logon SQL Server autenticado em vez da autenticação do Windows, adicione um logon ao servidor vinculado (consulte a seção anterior). Para fazer isso, use o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

No exemplo a seguir, há vários argumentos que são usados com o procedimento armazenado do sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :

-   "ADSI" é o argumento **rmtsvrname** , que é o nome do servidor vinculado criado no exemplo anterior.
-   "Fabrikam \\ administrador" é o argumento **locallogin** , que é o logon no servidor local e pode ser o logon SQL Server ou um usuário do Windows NT.
-   "CN = Administrator, OU = Sales, DC = activeds, DC = Fabrikam, DC = com" é o argumento **rmtuser** , que é o nome de usuário que você usa para se conectar porque **useself** é **false**.
-   "Secret \* \* 2000" é o **rmtpassword**, que é a senha associada a **rmtuser**

O comando [exec](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Consultando o serviço de diretório

Depois de criar um servidor vinculado, use uma instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar uma consulta ao serviço de diretório. A consulta SQL a seguir cria uma tabela virtual para manter os resultados da consulta usando a instrução [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) . A exibição que é criada é denominada "viewADContacts".

A primeira instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) define as informações que estão sendo consultadas do serviço de diretório e as mapeia para uma coluna na tabela. As informações entre colchetes indicam os dados que são colocados na tabela virtual. As informações que não estão entre colchetes indicam os dados recuperados do serviço de diretório. Observe que as informações que estão sendo recuperadas do serviço de diretório devem ser referenciadas pelo seu nome de exibição LDAP.

A próxima instrução é a instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você criou e uma instrução de consulta. A instrução de consulta contém os seguintes itens:

-   A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório. Será necessário usar o nome de exibição LDAP para indicar quais dados você está procurando.
-   A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas.
-   A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa. Neste exemplo, ele está procurando contatos.

A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) final é usada para escolher os resultados da exibição a ser exibida.


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




