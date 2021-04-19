---
title: Unindo dados heterogêneos
description: As organizações típicas armazenam dados em vários bancos de dados heterogêneos. Os dados de recursos humanos podem ser armazenados em SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório. Outros dados podem ser armazenados em formatos proprietários.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314609"
---
# <a name="joining-heterogeneous-data"></a>Unindo dados heterogêneos

As organizações típicas armazenam dados em vários bancos de dados heterogêneos. Os dados de recursos humanos podem ser armazenados em SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório. Outros dados podem ser armazenados em formatos proprietários.

Com o, SQL Server 7,0, ADSI e o provedor de OLE DB, é possível unir dados de Active Directory aos dados no SQL Server e criar uma exibição dos dados associados.

**Para unir dados de Active Directory com dados de SQL Server**

1.  Execute o **SQL Query Analyzer** (iniciar \| programas \| Microsoft SQL Server 7,0)
2.  Faça logon no computador SQL Server.
3.  Execute a seguinte linha (realçando-a e pressionando CTRL + E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    Nessa linha, os argumentos para o procedimento armazenado do sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) são os seguintes:

    -   "ADSI" é o argumento de **servidor** , que será o nome desse servidor vinculado.
    -   "Serviços Active Directorys" é o argumento **srvproduct** , que é o nome da fonte de dados OLE DB que você está adicionando como um servidor vinculado.
    -   "ADSDSOObject" é o argumento de **\_ nome do provedor** e indica que você está usando o provedor de OLE DB.
    -   "adsdatasource" é o **\_ argumento de fonte de dados**, que é o nome da fonte de dados conforme interpretado pelo provedor de OLE DB.

    Agora você pode usar o servidor vinculado para acessar Active Directory do SQL Server.

4.  O exemplo a seguir executa uma consulta usando a instrução [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você acabou de criar e uma instrução de consulta. A instrução de consulta contém os seguintes itens:

    -   A instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório. Será necessário usar o nome de exibição LDAP para indicar quais dados você está procurando.
    -   A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas.
    -   A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa. Neste exemplo, ele está procurando por usuários.

    Digite e execute:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    Você também pode usar o [DIALETO ADSI LDAP](ldap-dialect.md). Por exemplo:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    No exemplo anterior, a consulta LDAP tem quatro partes:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " é o nome distinto do servidor de diretório a ser pesquisado.
    -   "(& (objectCategory = Person) (objectClass = user))" é o filtro de pesquisa LDAP (consulte a [sintaxe do filtro de pesquisa](search-filter-syntax.md)).
    -   "Name, ADsPath" são os nomes (usando o formato de nome de exibição LDAP) dos atributos a serem recuperados.
    -   "Subtree" indica o [escopo](scope-of-query.md) da pesquisa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando e executando uma exibição](creating-and-executing-a-view.md)
</dt> </dl>

 

 




