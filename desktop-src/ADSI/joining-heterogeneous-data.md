---
title: Unindo dados heterogêneos
description: As organizações típicas armazenam dados em vários bancos de dados heterogêneos. Os dados de Recursos Humanos podem ser armazenados SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório . Outros dados podem ser armazenados em formatos proprietários.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409ac4e82d735f5099bb8846a59683075007c3fbdf56600bc5ae01e6863ffa2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656996"
---
# <a name="joining-heterogeneous-data"></a>Unindo dados heterogêneos

As organizações típicas armazenam dados em vários bancos de dados heterogêneos. Os dados de Recursos Humanos podem ser armazenados SQL Server, enquanto os dados de gerenciamento de conta são armazenados no diretório . Outros dados podem ser armazenados em formatos proprietários.

Com o SQL Server 7.0, a ADSI e o provedor OLE DB, é possível unir dados do Active Directory aos dados no SQL Server e criar uma exibição dos dados unidos.

**Para unir dados do Active Directory com SQL Server Dados**

1.  Executar o **SQL de Consulta (Iniciar** Programas \| Microsoft SQL Server \| 7.0)
2.  Faça logo SQL Server computador.
3.  Execute a seguinte linha (realçando-a e pressionando CTRL+E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    Nesta linha, os argumentos para o procedimento armazenado do sistema [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) são os seguinte:

    -   "ADSI" é o **argumento do** servidor, que será o nome desse servidor vinculado.
    -   "Serviços do Active Directory" é o **argumento srvproduct,** que é o nome da fonte OLE DB dados que você está adicionando como um servidor vinculado.
    -   "ADSDSOObject" é o argumento **de \_** nome do provedor e indica que você está usando o provedor OLE DB dados.
    -   "adsdatasource" é o argumento da fonte de dados **, \_** que é o nome da fonte de dados conforme interpretado pelo provedor OLE DB dados.

    Agora você pode usar o servidor vinculado para acessar o Active Directory do SQL Server.

4.  O exemplo a seguir executa uma consulta usando a [instrução OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Essa instrução tem dois argumentos: ADSI, que é o nome do servidor vinculado que você acabou de criar, e uma instrução de consulta. A instrução de consulta contém os seguintes itens:

    -   A [instrução SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório. Você precisará usar o nome de exibição LDAP para indicar quais dados você está procurando.
    -   A [instrução FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado do qual essas informações serão obtidas.
    -   A [instrução WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornece as condições de pesquisa. Neste exemplo, ele está pesquisando usuários.

    Digite e execute:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    Você também pode usar o dialeto [ADSI LDAP](ldap-dialect.md). Por exemplo:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    No exemplo anterior, a consulta LDAP tem quatro partes:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " é o nome diferenciado do servidor de diretório a ser pesquisado.
    -   "(&(objectCategory=Person)(objectClass=user))" é o filtro de pesquisa LDAP (consulte [Sintaxe de filtro de pesquisa).](search-filter-syntax.md)
    -   "name, adspath" são os nomes (usando o formato de nome de exibição LDAP) dos atributos a recuperar.
    -   "subárvore" indica [o escopo](scope-of-query.md) da pesquisa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando e executando uma exibição](creating-and-executing-a-view.md)
</dt> </dl>

 

 




