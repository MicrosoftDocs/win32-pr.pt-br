---
title: Classes auxiliares vinculadas estaticamente
description: Uma classe auxiliar vinculada estaticamente é aquela que está incluída no atributo auxiliaryClass ou systemAuxiliaryClass da definição classSchema de uma classe de objeto no esquema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- AD de classes auxiliares vinculadas estaticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634914"
---
# <a name="statically-linked-auxiliary-classes"></a>Classes auxiliares vinculadas estaticamente

Uma classe auxiliar vinculada estaticamente é aquela que está incluída no atributo **auxiliaryClass** ou **SystemAuxiliaryClass** da definição **classSchema** de uma classe de objeto no esquema. Isso significa que a classe auxiliar é parte de cada instância da classe à qual está associada.

Uma classe auxiliar pode ser vinculada estaticamente a uma classe de objeto quando a classe é definida, ou seja, quando seu objeto **classSchema** é adicionado ao contêiner de esquema. Essa é a única vez que o **systemAuxiliaryClass** pode ser usado; Depois que um objeto **classSchema** é criado, seu atributo **systemAuxiliaryClass** não pode ser modificado. Uma classe auxiliar que é vinculada estaticamente neste momento pode ter atributos obrigatórios (**mustHave**) e/ou opcionais (**mayHave**).

Um usuário com privilégios com as permissões necessárias para estender o esquema pode adicionar ou remover classes auxiliares do atributo **systemAuxiliaryClass** de um objeto **classSchema** existente. Isso adiciona ou remove a classe auxiliar de todas as instâncias existentes da classe de objeto. Uma classe auxiliar que é vinculada estaticamente neste momento pode ter atributos opcionais, mas não pode ter atributos obrigatórios. Isso ocorre porque pode haver instâncias existentes da classe Object; nesse caso, a adição de um novo atributo obrigatório criaria problemas. Um usuário privilegiado pode subseqüentemente remover uma classe auxiliar do atributo **auxiliaryClass** de um objeto **classSchema** .

 

 




