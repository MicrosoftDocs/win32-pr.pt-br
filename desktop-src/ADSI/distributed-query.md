---
title: Consulta Distribuída
description: Como a ADSI é um provedor OLE DB, ela pode participar da Consulta Distribuída introduzida no Microsoft SQL Server 7.0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- consultas ADSI, consulta distribuída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428697"
---
# <a name="distributed-query"></a>Consulta Distribuída

Como a ADSI é um provedor OLE DB, ela pode participar da Consulta Distribuída introduzida no Microsoft SQL Server 7.0. Veja a seguir possíveis cenários:

-   Ingressar objetos do Active Directory com SQL Server dados.
-   Atualizando SQL dados de objetos do Active Directory.
-   Criar junções de três ou quatro vias com outros provedores OLE DB dados. Por exemplo, Servidor de Índice, SQL Server e Active Directory.

O provedor OLE DB dá suporte a dois dialetos de comando, LDAP e SQL, para acessar o serviço de diretório e retornar resultados em um formulário tabular que pode ser consultado SQL Server consultas distribuídas.

**Para iniciar o analisador SQL consulta**

1.  Primeiro, abra o [SQL analisador](https://msdn.microsoft.com/library/Aa216983.aspx) de consulta no SQL Server que está vinculado ao serviço de diretório (consulte Criando um servidor vinculado).
2.  Executar o **SQL de Consulta (Iniciar** Programas \| Microsoft SQL Server \| 7.0)
3.  Faça logo SQL Server computador.
4.  Insira a SQL Consulta no painel Editor da janela de consulta.
5.  Execute a consulta pressionando F5.

As seções a seguir fornecem mais detalhes:

-   [Criando um servidor vinculado](#creating-a-linked-server)
-   [Criando um SQL Server logon autenticado](#creating-a-sql-server-authenticated-login)
-   [Consultando o serviço de diretório](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Criando um servidor vinculado

Para configurar uma junção distribuída em um Windows de diretório do Servidor 2000, crie um servidor vinculado. Para fazer isso, configurar o mapeamento ADSI usando o procedimento armazenado do sistema [sp \_ addlinkedserver.](https://msdn.microsoft.com/library/Aa259589.aspx) Este procedimento vincula um nome a um nome OLE DB provedor.

No exemplo a seguir, observe que há vários argumentos usados com o procedimento armazenado do sistema [sp \_ addlinkedserver:](https://msdn.microsoft.com/library/Aa259589.aspx)

-   "ADSI" é o **argumento do** servidor e será o nome desse servidor vinculado.
-   "Active Directory Services 2.5" é o argumento **srvproduct,** que é o nome da fonte de dados OLE DB que você está adicionando como um servidor vinculado.
-   "ADSDSOObject" é o argumento **de \_ nome do** provedor.
-   "adsdatasource" é **\_** o argumento da fonte de dados, que é o nome da fonte de dados conforme interpretado pelo provedor OLE DB dados.

O [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Para Windows logon autenticados, o auto mapeamento é suficiente para acessar o diretório com SQL Server delegação de segurança. Como o auto mapeamento é criado por padrão para servidores vinculados criados por meio de [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), nenhum outro mapeamento de logon é necessário.

Para SQL Server logon autenticado, você pode configurar logons e senhas adequados para se conectar ao serviço de diretório usando o procedimento armazenado do sistema [ \_ sp addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

> [!Note]  
> Quando possível, use a Autenticação do Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Criando um SQL Server logon autenticado

Se você preferir usar um logon SQL Server autenticado em vez de Windows autenticação, adicione um logon ao servidor vinculado (consulte a seção anterior). Para fazer isso, use o procedimento armazenado do sistema [ \_ sp addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

No exemplo a seguir, há vários argumentos que são usados com o procedimento armazenado do sistema [sp \_ addlinkedsrvlogin:](https://msdn.microsoft.com/library/Aa259581.aspx)

-   "ADSI" é o **argumento rmtsvrname,** que é o nome do servidor vinculado criado no exemplo anterior.
-   "Administrador da Fabrikam" é o argumento \\ **locallogin,** que é o logon no servidor local e pode ser o logon SQL Server ou um Windows NT usuário.
-   "CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" é o argumento **rmtuser,** que é o nome de usuário que você usa para se conectar porque **useself** é **false.**
-   "secret \* \* 2000" é **a rmtpassword**, que é a senha associada ao **rmtuser**

O [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) é usado para executar procedimentos armazenados do sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Consultando o serviço de diretório

Depois de criar um servidor vinculado, use uma instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) para enviar uma consulta ao Serviço de Diretório. A consulta SQL a seguir cria uma tabela virtual para manter os resultados da consulta usando a [instrução CREATE VIEW.](https://msdn.microsoft.com/library/Aa258253.aspx) A exibição criada é denominada "viewADContacts".

A primeira [instrução SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) define as informações que estão sendo consultadas do serviço de diretório e as mapeia para uma coluna na tabela. As informações entre colchetes indicam os dados que são colocados na tabela virtual. As informações que não estão entre colchetes indicam os dados recuperados do serviço de diretório. Observe que as informações que estão sendo recuperadas do serviço de diretório devem ser referenciadas por seu nome de exibição LDAP.

A próxima instrução é a [instrução OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você criou e uma instrução de consulta. A instrução de consulta contém os seguintes itens:

-   A [instrução SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório. Você precisará usar o nome de exibição LDAP para indicar quais dados você está procurando.
-   A [instrução FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado do qual essas informações serão obtidas.
-   A [instrução WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornece as condições de pesquisa. Neste exemplo, ele está procurando contatos.

A [instrução SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) final é usada para selecionar os resultados da exibição a ser exibida.


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



 

 




