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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="ec45e-103">Criando uma junção heterogênea entre SQL Server & Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec45e-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="ec45e-104">Todos os funcionários da Fabrikam Corporation são examinados a cada seis meses.</span><span class="sxs-lookup"><span data-stu-id="ec45e-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="ec45e-105">As classificações de revisão são armazenadas no banco de dados de recursos humanos no SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec45e-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="ec45e-106">Para criar uma exibição desses dados, Joe Worden, o administrador corporativo, deve primeiro criar uma tabela de revisão de desempenho de funcionário.</span><span class="sxs-lookup"><span data-stu-id="ec45e-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="ec45e-107">No SQL Query Analyzer, Joe vai criar uma tabela chamada EMP \_ Review que conterá três colunas para manter o nome do funcionário, a data da revisão e a classificação que o funcionário recebeu.</span><span class="sxs-lookup"><span data-stu-id="ec45e-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="ec45e-108">Joe pode inserir alguns registros.</span><span class="sxs-lookup"><span data-stu-id="ec45e-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="ec45e-109">Agora Joe pode unir o Active Directory objetos de usuário à tabela SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec45e-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="ec45e-110">Neste exemplo, a instrução [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contém a lista de dados que serão obtidos do serviço de diretório e SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ec45e-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="ec45e-111">A instrução [from](https://msdn.microsoft.com/library/Aa258869.aspx) contém o nome do servidor de diretório vinculado para o qual essas informações serão obtidas, nesse caso, viewADUsers.</span><span class="sxs-lookup"><span data-stu-id="ec45e-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="ec45e-112">A instrução [Where](https://msdn.microsoft.com/library/Aa260674.aspx) fornece os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ec45e-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="ec45e-113">Neste exemplo, ele está pesquisando pelo nome no serviço de diretório, que é definido como o nome de usuário SQL inserido na tarefa anterior.</span><span class="sxs-lookup"><span data-stu-id="ec45e-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="ec45e-114">O comando anterior Obtém o resultado de SQL Server e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec45e-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="ec45e-115">AdsPath e title são de Active Directory, enquanto userName, ReviewDate e rating são da tabela SQL.</span><span class="sxs-lookup"><span data-stu-id="ec45e-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="ec45e-116">Ele pode até mesmo criar outra exibição para essa junção.</span><span class="sxs-lookup"><span data-stu-id="ec45e-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




