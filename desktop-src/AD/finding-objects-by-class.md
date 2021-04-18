---
title: Localizando objetos por classe
description: As consultas de pesquisa típicas para uma classe de objeto específica.
ms.assetid: 1805f98a-7e6b-4b4a-b173-dfb5d17e539a
ms.tgt_platform: multiple
keywords:
- Localizando objetos por AD de classe
- Active Directory, usando, pesquisando, por classe
- ANÚNCIO de objeto, pesquisando por classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172c8b150090fae83aee1cf3e0f6a63a0e21dec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756494"
---
# <a name="finding-objects-by-class"></a>Localizando objetos por classe

As consultas de pesquisa típicas para uma classe de objeto específica. O exemplo de código a seguir pesquisa computadores com o local em Compilando 7N.


```C++
(&(objectCategory=computer)(location=Building 7N))
```



Considere por que o **objectClass** não é usado. Não use **objectClass** sem outra comparação que contenha um atributo indexado. Atributos de índice podem aumentar a eficiência de uma consulta. O atributo **objectClass** tem valores múltiplos e não indexados. Para especificar o tipo ou a classe de um objeto, use **objectCategory**.

Menos eficiente:


```C++
(objectClass=computer)
```



Mais eficiente:


```C++
(objectCategory=computer)
```



Lembre-se de que há alguns casos em que uma combinação de **objectClass** e **objectCategory** deve ser usada. A classe de usuário e a classe de contato devem ser especificadas da seguinte maneira.


```C++
(&(objectClass=user)(objectCategory=person))
 
(&(objectClass=contact)(objectCategory=person))
```



Lembre-se de que você pode pesquisar por usuários e contatos com o seguinte.


```C++
(objectCategory=person)
```



 

 




