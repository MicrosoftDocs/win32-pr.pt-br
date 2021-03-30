---
title: Localizando objetos por nome
description: A maioria dos objetos no Active Directory Domain Services usar a propriedade CN como seu atributo de nomenclatura.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, pesquisando, por nome
- ANÚNCIO de objeto, pesquisando por nome
- Localizando objetos por nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634941"
---
# <a name="finding-objects-by-name"></a>Localizando objetos por nome

A maioria dos objetos no Active Directory Domain Services usar a propriedade **CN** como seu atributo de nomenclatura. Alguns objetos, no entanto, usam um atributo de nomenclatura diferente de **CN**. Por exemplo, um controlador de domínio usa a propriedade **domainDns** para o atributo de nomenclatura e uma unidade organizacional usa a propriedade **OrganizationalUnit** para o atributo de nomenclatura. Para evitar a utilização de um atributo de nomenclatura diferente para diferentes tipos de objeto, a propriedade **Name** , que contém o nome distinto relativo do objeto, deve ser usada para pesquisar objetos pelo nome.

## <a name="examples"></a>Exemplos

Os exemplos de código a seguir mostram diferentes cadeias de caracteres de consulta que podem ser usadas para localizar objetos por nome.

A cadeia de caracteres de consulta a seguir localiza todos os objetos com um nome que começa com "Jeff".


```C++
(name=Jeff*)
```



A cadeia de caracteres de consulta a seguir localiza todos os objetos de computador com um nome que começa com "concedido" ou "Corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



A cadeia de caracteres de consulta a seguir localiza todos os usuários e com um nome que começa com "Karen" ou "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




