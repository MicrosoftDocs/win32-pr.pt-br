---
title: Consultando objetos de esquema de categoria 1 ou 2
description: O atributo systemFlags dos objetos attributeSchema e classSchema é um bitmask inteiro que contém sinalizadores que indicam qualidades de sistema adicionais do atributo ou da classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Consultando o AD de objetos de esquema de categoria 1 ou 2
- ANÚNCIO de objeto, consultando objetos de esquema de categoria 1 ou 2
- AD do esquema, consultando objetos de esquema de categoria 1 ou 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293888"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Consultando objetos de esquema de categoria 1 ou 2

O atributo **systemFlags** dos objetos **attributeSchema** e **classSchema** é um bitmask inteiro que contém sinalizadores que indicam qualidades de sistema adicionais do atributo ou da classe. A [**enumeração \_ \_ enum do ADS SYSTEMFLAG**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contém valores que correspondem aos bits que você pode definir no atributo **systemFlags** . Há bits **systemFlags** adicionais que você não pode definir, como o bit 0x10, que indica se o atributo ou a classe é a categoria 1 ou a categoria 2. O bit 0x10 é definido para objetos Category 1, que são as classes e os atributos incluídos no esquema base incluído no sistema. O bit não está definido para atributos e classes da categoria 2, que são extensões para o esquema. Se não existir nenhuma propriedade **systemFlags** em um objeto **attributeSchema** ou **classSchema** , ela será a categoria 2.

O **\_ bit de regra de correspondência LDAP \_ \_ \_ e** a regra de correspondência podem ser usados para pesquisar objetos que tenham o sinalizador 0x10 definido no atributo **systemFlags** . Para obter mais informações, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Consultando a categoria 1

A cadeia de consulta a seguir procura atributos da categoria 1 (objetos **attributeSchema** com o bit 0x10 definido na propriedade **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Lembre-se de que, no exemplo acima, a sintaxe de consulta LDAP requer valores decimais; Portanto, o valor hexadecimal do sinalizador deve ser convertido em decimal. Nesse caso, a categoria de 1 bit é 0x10, portanto, o valor do filtro deve ser especificado como 16.

## <a name="querying-for-category-2"></a>Consultando a categoria 2

A cadeia de consulta a seguir procura atributos da categoria 2 (objetos **attributeSchema** que não têm o bit 0x10 definido na propriedade **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Lembre-se de que essa consulta também retorna objetos **attributeSchema** que não têm uma propriedade **systemFlags** e, portanto, implicitamente não têm o sinalizador especificado definido.

 

 