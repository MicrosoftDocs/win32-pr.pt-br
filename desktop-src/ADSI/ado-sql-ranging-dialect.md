---
title: Dialeto de intervalo de SQL do ADO
description: Ao usar o ADO (ActiveX Directory Objects), usando o dialeto SQL, aspas simples (') devem ser usadas em volta do atributo e do especificador de intervalo.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- ADSI de dialeto SQL do ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811200"
---
# <a name="ado-sql-ranging-dialect"></a><span data-ttu-id="0c744-104">Dialeto de intervalo de SQL do ADO</span><span class="sxs-lookup"><span data-stu-id="0c744-104">ADO SQL Ranging Dialect</span></span>

<span data-ttu-id="0c744-105">Ao usar o ADO (ActiveX Directory Objects), usando o dialeto SQL, aspas simples (') devem ser usadas em volta do atributo e do especificador de intervalo.</span><span class="sxs-lookup"><span data-stu-id="0c744-105">When using the ActiveX Directory Objects (ADO), using the SQL dialect, single quotation marks (') must be used around the attribute and range specifier.</span></span> <span data-ttu-id="0c744-106">Veja a seguir um exemplo do dialeto SQL do ADO.</span><span class="sxs-lookup"><span data-stu-id="0c744-106">The following is an example of the ADO SQL dialect.</span></span>


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




