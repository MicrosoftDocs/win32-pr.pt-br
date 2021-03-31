---
title: Dialeto de intervalo de LDAP do ADO
description: Ao usar ADO (ActiveX Directory Objects) com o dialeto LDAP, o atributo e o especificador de intervalo não exigem aspas.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- ADSI de dialeto do ADO LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822244"
---
# <a name="ado-ldap-ranging-dialect"></a>Dialeto de intervalo de LDAP do ADO

Ao usar ADO (ActiveX Directory Objects) com o dialeto LDAP, o atributo e o especificador de intervalo não exigem aspas.

Veja a seguir um exemplo do dialeto ADO LDAP.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




