---
title: O esquema abstrato
description: O contêiner de esquema contém todos os objetos classSchema e attributeSchema que definem as classes e atributos que podem existir em uma floresta de diretórios.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- O AD de esquema abstrato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b46e4fefd52e786829e051a14714d2fec118b2ad42cdd95afcaa78b098b0f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182777"
---
# <a name="the-abstract-schema"></a>O esquema abstrato

O contêiner de esquema contém todos os objetos **classSchema** e **attributeSchema** que definem as classes e atributos que podem existir em uma floresta de diretórios. O contêiner de esquema também contém um objeto chamado Aggregate da **classe subSchema**. Esse **objeto subSchema** é conhecido como o esquema abstrato.

O esquema abstrato contém um subconjunto dos dados armazenados nos objetos **classSchema** e **attributeSchema.** Sua finalidade é fornecer um mecanismo simples e eficiente para recuperar os elementos usados com frequência das definições de classe e atributo. Por exemplo, para recuperar os atributos opcionais e obrigatórios de uma classe de objeto, a bind a vários objetos para coletar os valores **mayContain**, **mustContain**, **systemMayContain** e **systemMustContain** da classe e todas as suas superclasses, bem como de todas as classes auxiliares da classe e suas superclasses. O esquema abstrato coleta convenientemente todos esses dados em um único objeto.

Assim como com qualquer objeto no Active Directory Domain Services, você pode se vincular ao objeto **subSchema** e ler seus atributos, analisar os valores de cadeia de caracteres para recuperar os dados desejados. No entanto, a ADSI fornece um conjunto de interfaces que facilitam muito a leitura do esquema abstrato. Para obter mais informações, consulte [Lendo o esquema abstrato](reading-the-abstract-schema.md).

A tabela a seguir lista os principais atributos de um **objeto subSchema.**



| Atributo                 | Descrição                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Um atributo com vários valores que contém cadeias de caracteres que representam cada atributo no esquema. Cada valor contém **o attributeID**, **lDAPDisplayName**, **attributeSyntax,** **rangeLower,** **rangeUpper** e um item que indica se o atributo pode ter vários valores. |
| **extendedAttributeInfo** | Um atributo com vários valores que contém cadeias de caracteres que representam dados adicionais para cada atributo. Cada valor contém **attributeID,** **lDAPDisplayName,** **schemaIDGUID** e **attributeSecurityGUID.**                                                                          |
| **extendedClassInfo**     | Um atributo com vários valores que contém cadeias de caracteres que representam dados adicionais para cada classe. Cada valor contém **o governsID,** **lDAPDisplayName** e **schemaIDGUID** da classe .                                                                                              |
| **objectClasses**         | Um atributo com valores múltiplos que contém cadeias de caracteres que representam cada classe no esquema. Cada valor contém **o governsID**, **lDAPDisplayName**, **mustContain**, **mayContain** e assim por diante.                                                                                           |



 

 

 




