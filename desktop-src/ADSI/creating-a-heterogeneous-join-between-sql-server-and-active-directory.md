---
title: Criando uma junção heterogênea entre SQL Server & Active Directory
description: Todos os funcionários da Fabrikam Corporation são examinados a cada seis meses.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103917013"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Criando uma junção heterogênea entre SQL Server & Active Directory

Todos os funcionários da Fabrikam Corporation são examinados a cada seis meses. As classificações de revisão são armazenadas no banco de dados de recursos humanos no SQL Server. Para criar uma exibição desses dados, Joe Worden, o administrador corporativo, deve primeiro criar uma tabela de revisão de desempenho de funcionário.

No SQL Query Analyzer, Joe vai criar uma tabela chamada EMP \_ Review que conterá três colunas para manter o nome do funcionário, a data da revisão e a classificação que o funcionário recebeu.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Joe pode inserir alguns registros.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Agora Joe pode unir o Active Directory objetos de usuário à tabela SQL Server.

Neste exemplo, a instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório e SQL Server. A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas, nesse caso, viewADUsers. A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa. Neste exemplo, ele está pesquisando pelo nome no serviço de diretório, que é definido como o nome de usuário SQL inserido na tarefa anterior.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



O comando anterior Obtém o resultado de SQL Server e Active Directory. AdsPath e title são de Active Directory, enquanto userName, ReviewDate e rating são da tabela SQL. Ele pode até mesmo criar outra exibição para essa junção.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




