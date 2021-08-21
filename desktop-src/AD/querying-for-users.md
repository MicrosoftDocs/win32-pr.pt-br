---
title: Consultando usuários
description: Para consultar um usuário, a consulta deve conter a expressão de pesquisa \ 0034;( (usuário objectClass) (objectCategory person)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- users AD , consultando usuários
- Active Directory, usando usuários, consultando usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025314"
---
# <a name="querying-for-users"></a>Consultando usuários

Para consultar um usuário, a consulta deve conter a expressão de pesquisa "(&(objectClass=user)(objectCategory=person))".

Como a classe de computador é uma subclasse de usuário, uma consulta que contém somente (objectClass=user) retornaria objetos de usuário e objetos de computador. Além disso, a categoria de objeto do objeto de usuário é pessoa (não usuário); portanto, a expressão (objectCategory=user) não retorna nenhum usuário. Se você usar a expressão (objectCategory=person), a consulta retornará objetos de usuário e objetos de contato.

Os usuários podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como na raiz do domínio. Isso significa que os usuários podem estar em vários locais na hierarquia de diretórios. Você pode executar uma pesquisa profunda para "(objectCategory=user)" para localizar todos os usuários em um contêiner, unidade organizacional, domínio, árvore de domínio ou floresta— dependendo do objeto ao que o ponteiro [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que você está usando está vinculado.

 

 