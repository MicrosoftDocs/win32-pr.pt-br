---
title: Localizar objetos por nome
description: A maioria dos objetos Active Directory Domain Services a propriedade cn como seu atributo de nomen entre eles.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, pesquisando, por nome
- object AD , pesquisando por nome
- Localizar objetos por nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60624c62e9d28d35805af3c98f551a19f44edf9e27369cf7ded9e87621491cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189176"
---
# <a name="finding-objects-by-name"></a>Localizar objetos por nome

A maioria dos objetos Active Directory Domain Services a **propriedade cn** como seu atributo de nomen entre eles. Alguns objetos, no entanto, usam um atributo de nomenu diferente de **cn**. Por exemplo, um controlador de domínio usa a propriedade **domainDNS** para o atributo de nomeação e uma unidade organizacional usa a propriedade **organizationalUnit** para o atributo de nomenv. Para evitar a precisar usar um atributo de  nomeação diferente para diferentes tipos de objeto, a propriedade name, que contém o nome diferenciado relativo do objeto, deve ser usada para pesquisar objetos por nome.

## <a name="examples"></a>Exemplos

Os exemplos de código a seguir mostram cadeias de caracteres de consulta diferentes que podem ser usadas para encontrar objetos por nome.

A cadeia de caracteres de consulta a seguir localiza todos os objetos com um nome que começa com "Jeff".


```C++
(name=Jeff*)
```



A cadeia de caracteres de consulta a seguir localiza todos os objetos de computador com um nome que começa com "leased" ou "corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



A cadeia de caracteres de consulta a seguir localiza todos os usuários e com um nome que começa com "Paulo" ou "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




