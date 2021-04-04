---
title: Determinando um tipo de atributo
description: O atributo systemFlags de um objeto attributeSchema contém um conjunto de sinalizadores que indicam várias qualidades do objeto de atributo, como, por exemplo, se o atributo é construído ou não replicado.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinando um tipo de atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007326"
---
# <a name="determining-an-attribute-type"></a>Determinando um tipo de atributo

O atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) de um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contém um conjunto de sinalizadores que indicam várias qualidades do objeto de atributo, como, por exemplo, se o atributo é construído ou não replicado. A tabela a seguir lista os sinalizadores do atributo **systemFlags** que afetam o tipo de armazenamento do atributo. 

| Valor do sinalizador | Descrição                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Se esse sinalizador estiver presente no atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , o atributo não será replicado. |
| 0x00000004 | Se esse sinalizador estiver presente no atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , o atributo será construído.    |



 

É possível construir uma cadeia de caracteres de consulta que possa ser usada para consultar atributos construídos ou não replicados. Por exemplo, a cadeia de caracteres de consulta a seguir localiza todos os objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) não replicados. Lembre-se de que a cadeia de caracteres de consulta requer o equivalente Decimal do valor, não o equivalente hexadecimal do valor. Para obter mais informações sobre o OID de regra de correspondência usado por essa cadeia de caracteres de consulta, consulte [como especificar valores de comparação](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



O atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) do objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define se um atributo é indexado; um atributo indexado tem um valor de 1, um atributo não indexado tem um valor de 0. Por exemplo, a cadeia de caracteres de consulta a seguir localiza os objetos **attributeSchema** que representam os atributos indexados.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



O atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) do objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define se um atributo é replicado para o catálogo global. Esse atributo tem um valor de **true** se o atributo for um membro do catálogo global ou **false** se os atributos não estiverem no catálogo global. Por exemplo, a cadeia de caracteres de consulta a seguir pesquisa os objetos **attributeSchema** que são replicados para o catálogo global.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 