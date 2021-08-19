---
title: Criando e executando uma exibição
description: Você pode criar uma exibição para os dados obtidos do Active Directory. Esteja ciente de que apenas a definição de exibição é armazenada SQL Server, e não o conjunto de resultados real. Portanto, você pode obter um resultado diferente ao invocar a exibição posteriormente.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c4676154ea32dd06e39498e9f943b55d8dbf39694ab9c1005e942cad85f7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082720"
---
# <a name="creating-and-executing-a-view"></a>Criando e executando uma exibição

Você pode criar uma exibição para os dados obtidos do Active Directory. Esteja ciente de que apenas a definição de exibição é armazenada SQL Server, e não o conjunto de resultados real. Portanto, você pode obter um resultado diferente ao invocar a exibição posteriormente.

O exemplo de código a seguir mostra como criar uma exibição.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Use o código a seguir para invocar uma exibição.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma junção heterogênea entre o SQL Server e o Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




