---
description: As funções SetNamedSecurityInfo e SetSecurityInfo são suportadas pela propagação automática de ACEs (entradas de controle de acesso) herdáveis.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagação automática de ACEs herdáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257c038174549eebb8d960f8f4bc0601f95a928478e2a783f93f4a1444a22d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783713"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagação automática de ACEs herdáveis

As [**funções SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) são suportadas pela propagação automática de ACEs (entradas de controle [*de acesso)*](/windows/desktop/SecGloss/a-gly) herdáveis. Por exemplo, se você usar essas funções para adicionar uma ACE herdável a um diretório em um NTFS, o sistema aplicará a ACE conforme apropriado às ACLs [*(listas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) de quaisquer subdireários ou arquivos existentes.

AcEs aplicadas diretamente têm precedência sobre ACEs herdadas. O sistema implementa essa precedência colocando ACEs aplicadas diretamente à frente das ACEs herdadas em uma DACL (lista de controle [*de*](/windows/desktop/SecGloss/d-gly) acesso discricionário). Quando você chama as funções [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para definir as informações de segurança de um objeto, o sistema impõe o modelo de herança atual nas ACLs de todos os objetos na hierarquia abaixo do objeto de destino. Para objetos que foram convertidos no modelo de herança atual, os bits ES DACL AUTO INHERITED e ES SACL AUTO INHERITED são definidos no campo de controle do descritor de segurança do \_ \_ \_ \_ \_ \_ objeto. [](/windows/desktop/SecGloss/s-gly)

Quando você cria um novo descritor de segurança que reflete o modelo de herança atual, é preciso ter cuidado para não alterar a semântica do descritor de segurança. Dessa forma, as ACEs de permitir e negar nunca são movidas em relação umas às outras. Se tal movimentação for necessária (por exemplo, para colocar todas as ACEs não herheritadas na frente de uma ACL), a ACL será marcada como protegida para evitar a alteração semântica.

O sistema usa as seguintes regras ao propagar ACEs herdadas para objetos filho:

-   Se um objeto filho sem DACL herdar uma ACE, o resultado será um objeto filho com uma DACL que contém apenas a ACE herdada.
-   Se um objeto filho com uma DACL vazia herdar uma ACE, o resultado será um objeto filho com uma DACL que contém apenas a ACE herdada.
-   Se você remover uma ACE herdável de um objeto pai, a herança automática removerá todas as cópias da ACE herdadas por objetos filho.
-   Se a herança automática resulta na remoção de todas as ACEs da DACL de um objeto filho, o objeto filho tem uma DACL vazia em vez de nenhuma DACL.

Essas regras podem ter o resultado inesperado de converter um objeto sem DACL em um objeto com uma DACL vazia. Um objeto sem DACL permite acesso completo, mas um objeto com uma DACL vazia não permite acesso. Como um exemplo de como essas regras podem criar uma DACL vazia, suponha que você adicione uma ACE herdável ao objeto raiz de uma árvore de objetos. A herança automática propaga o ACE herdável para todos os objetos na árvore. Objetos filho que iniciaram sem DACL agora têm uma DACL com a ACE herdada. Se você remover o ACE herdável do objeto raiz, o sistema propaga automaticamente a alteração para os objetos filho. Objetos filho que começaram sem DACL (permitindo acesso completo) agora têm uma DACL vazia (sem acesso).

Para garantir que um objeto filho sem DACL não seja afetado por ACEs herdáveis, de definir o sinalizador ES DACL PROTECTED no descritor \_ \_ de segurança do objeto.

Para obter informações sobre como criar corretamente uma DACL, consulte [Criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
