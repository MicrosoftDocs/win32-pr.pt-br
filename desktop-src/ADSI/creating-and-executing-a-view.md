---
title: Criando e executando uma exibição
description: Você pode criar uma exibição para os dados obtidos do Active Directory. Lembre-se de que apenas a definição de exibição é armazenada em SQL Server, e não o conjunto de resultados real. Portanto, você pode obter um resultado diferente ao invocar a exibição mais tarde.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363655"
---
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="a72bd-105">Criando e executando uma exibição</span><span class="sxs-lookup"><span data-stu-id="a72bd-105">Creating and Executing a View</span></span>

<span data-ttu-id="a72bd-106">Você pode criar uma exibição para os dados obtidos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a72bd-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="a72bd-107">Lembre-se de que apenas a definição de exibição é armazenada em SQL Server, e não o conjunto de resultados real.</span><span class="sxs-lookup"><span data-stu-id="a72bd-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="a72bd-108">Portanto, você pode obter um resultado diferente ao invocar a exibição mais tarde.</span><span class="sxs-lookup"><span data-stu-id="a72bd-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="a72bd-109">O exemplo de código a seguir mostra como criar uma exibição.</span><span class="sxs-lookup"><span data-stu-id="a72bd-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="a72bd-110">Use o código a seguir para invocar uma exibição.</span><span class="sxs-lookup"><span data-stu-id="a72bd-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="a72bd-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a72bd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a72bd-112">Criando uma junção heterogênea entre SQL Server e Active Directory</span><span class="sxs-lookup"><span data-stu-id="a72bd-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




