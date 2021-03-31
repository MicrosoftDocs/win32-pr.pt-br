---
title: Consultando usuários
description: Para consultar um usuário, a consulta deve conter a expressão de pesquisa \ 0034;( (usuário objectClass) (pessoa da objectCategory)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- AD de usuários, consultando usuários
- Active Directory, usando, usuários, consultando usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640389"
---
# <a name="querying-for-users"></a>Consultando usuários

Para consultar um usuário, a consulta deve conter a expressão de pesquisa "(& (objectClass = user) (objectCategory = Person))".

Como a classe Computer é uma subclasse de User, uma consulta contendo somente (objectClass = user) retornará objetos User e Computer. Além disso, a categoria de objeto do objeto de usuário é Person (não User); Portanto, a expressão (objectCategory = user) não retorna nenhum usuário. Se você usar a expressão (objectCategory = Person), a consulta retornará objetos de usuário e objetos de contato.

Os usuários podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio. Isso significa que os usuários podem estar em vários locais na hierarquia de diretórios. Você pode executar uma pesquisa profunda para "(objectCategory = user)" para localizar todos os usuários em um contêiner, unidade organizacional, domínio, árvore de domínio ou floresta — dependendo do objeto que o ponteiro do [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que você está usando está vinculado.

 

 