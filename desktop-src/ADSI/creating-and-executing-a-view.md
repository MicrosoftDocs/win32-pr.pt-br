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
# <a name="creating-and-executing-a-view"></a>Criando e executando uma exibição

Você pode criar uma exibição para os dados obtidos do Active Directory. Lembre-se de que apenas a definição de exibição é armazenada em SQL Server, e não o conjunto de resultados real. Portanto, você pode obter um resultado diferente ao invocar a exibição mais tarde.

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

[Criando uma junção heterogênea entre SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




