---
title: O esquema abstrato
description: O contêiner de esquema contém todos os objetos classSchema e attributeSchema que definem as classes e os atributos que podem existir em uma floresta de diretório.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- O AD do esquema abstrato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004892"
---
# <a name="the-abstract-schema"></a>O esquema abstrato

O contêiner de esquema contém todos os objetos **classSchema** e **attributeSchema** que definem as classes e os atributos que podem existir em uma floresta de diretório. O contêiner de esquema também contém um objeto chamado agregação de **subesquema** de classe. Esse objeto de **subesquema** é conhecido como esquema abstrato.

O esquema abstrato contém um subconjunto dos dados armazenados nos objetos **classSchema** e **attributeSchema** . Seu objetivo é fornecer um mecanismo simples e eficiente para recuperar os elementos usados com frequência das definições de classe e de atributo. Por exemplo, para recuperar os atributos opcionais e obrigatórios de uma classe de objeto, associe-se a vários objetos para coletar os valores **mayContain**, **mustContain**, **systemMayContain** e **systemMustContain** da classe e de todas as suas superclasses, bem como de quaisquer classes auxiliares da classe e suas superclasses. O esquema abstrato coleta convenientemente todos esses dados em um único objeto.

Assim como ocorre com qualquer objeto no Active Directory Domain Services, você pode associar ao objeto de **subesquema** e ler seus atributos, analisando os valores da cadeia de caracteres para recuperar os dados desejados. No entanto, a ADSI fornece um conjunto de interfaces que tornam muito mais fácil ler o esquema abstrato. Para obter mais informações, consulte [lendo o esquema abstrato](reading-the-abstract-schema.md).

A tabela a seguir lista os principais atributos de um objeto de **subesquema** .



| Atributo                 | Descrição                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Um atributo com valores múltiplos que contém cadeias de caracteres que representam cada atributo no esquema. Cada valor contém **AttributeID**, **lDAPDisplayName**, **attributeSyntax**, **RangeLower**, **rangeUpper** e um item que indica se o atributo pode ter vários valores. |
| **extendedAttributeInfo** | Um atributo com valores múltiplos que contém cadeias de caracteres que representam dados adicionais para cada atributo. Cada valor contém **AttributeID**, **lDAPDisplayName**, **schemaIDGUID** e **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Um atributo com valores múltiplos que contém cadeias de caracteres que representam dados adicionais para cada classe. Cada valor contém o **governsID**, **lDAPDisplayName** e **schemaIDGUID** da classe.                                                                                              |
| **objectclasss**         | Um atributo com valores múltiplos que contém cadeias de caracteres que representam cada classe no esquema. Cada valor contém **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain** e assim por diante.                                                                                           |



 

 

 




