---
title: Classes estruturais, abstratas e auxiliares
description: O atributo objectClassCategory de um objeto classSchema pode ter um valor, conforme listado na tabela a seguir, que indica se a classe é estrutural, abstrata ou auxiliar.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- AD de classes estruturais, abstratas e auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393c08f5c26690d5b08b76dfea8ab4ff2833c94851a10ddcea2a69209279fbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024704"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Classes estruturais, abstratas e auxiliares

O atributo **objectClassCategory** de um objeto **classSchema** pode ter um valor, conforme listado na tabela a seguir, que indica se a classe é estrutural, abstrata ou auxiliar.



| Valor | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Uma classe estrutural, que é o único tipo de classe que pode ter instâncias em Active Directory Domain Services. Uma classe estrutural pode ser uma subclasse de uma classe abstrata ou estrutural. Uma classe estrutural pode incluir qualquer número de classes auxiliares em sua definição.                                                                                                                                                                                                                                           |
| 2     | Uma classe abstrata, que é um modelo usado para derivar novas classes abstratas, auxiliares e estruturais. Uma classe abstract só pode ser uma subclasse de uma classe abstract. Classes abstratas não podem ser instanciadas em Active Directory Domain Services. Uma classe abstrata pode incluir qualquer número de classes auxiliares em sua definição.                                                                                                                                                                                   |
| 3     | Uma classe auxiliar, que pode ser incluída na definição de uma classe estrutural, abstrata ou auxiliar. nesse caso, os valores **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** da classe auxiliar são adicionados a esses da classe... Uma classe auxiliar pode ser uma subclasse de uma classe abstrata ou auxiliar. As classes auxiliares não podem ser instanciadas no Active Directory Domain Services. Uma classe auxiliar pode incluir qualquer número de classes auxiliares em sua definição. |



 

Não confunda o **objectClassCategory** com uma [categoria de objeto](object-class-and-object-category.md).

 

 




