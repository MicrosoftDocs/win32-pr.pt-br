---
title: Criando uma junção heterogênea entre SQL Server & Active Directory
description: Todos os funcionários da Fabrikam Corporation são revisados a cada seis meses.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840286"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Criando uma junção heterogênea entre SQL Server & Active Directory

Todos os funcionários da Fabrikam Corporation são revisados a cada seis meses. As classificações de revisão são armazenadas no banco de dados de Recursos Humanos SQL Server. Para criar uma exibição desses dados, Joe Worden, o administrador corporativo, deve primeiro criar uma tabela de revisão de desempenho de funcionários.

No Analisador de Consultas do SQL, Joe criará uma tabela chamada EMP REVIEW que conterá três colunas para conter o nome do funcionário, a data da revisão e a classificação que o funcionário \_ recebeu.


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



Agora, Joe pode unir os objetos de usuário do Active Directory à tabela SQL Server dados.

Neste exemplo, a [instrução SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório e SQL Server. A [instrução FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado do qual essas informações serão obtidas, nesse caso, viewADUsers. A [instrução WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornece as condições de pesquisa. Neste exemplo, ele está pesquisando pelo nome no serviço de diretório, que é definido como o SQL userName inserido na tarefa anterior.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



O comando anterior obtém o resultado do SQL Server e do Active Directory. AdsPath e title são do Active Directory, enquanto userName, ReviewDate e Rating são da tabela SQL dados. Ele pode até mesmo criar outra exibição para essa junção.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




