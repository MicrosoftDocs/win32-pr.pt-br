---
description: As funções SetNamedSecurityInfo e SetSecurityInfo dão suporte à propagação automática de ACEs (entradas de controle de acesso) herdáveis.
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Propagação automática de ACEs herdáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fab03c73a1c926468e46a0d0492e512dab42af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172320"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Propagação automática de ACEs herdáveis

As funções [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) dão suporte à propagação automática de ACEs (entradas de [*controle de acesso*](/windows/desktop/SecGloss/a-gly) ) herdáveis. Por exemplo, se você usar essas funções para adicionar uma ACE herdável a um diretório em um NTFS, o sistema aplicará a ACE conforme apropriado às ACLs ( [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de quaisquer subdiretórios ou arquivos existentes.

ACEs aplicadas diretamente têm precedência sobre ACEs herdadas. O sistema implementa essa precedência colocando ACEs diretamente aplicadas à frente de ACEs herdadas em uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ). Quando você chama as funções [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) e [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para definir as informações de segurança de um objeto, o sistema impõe o modelo de herança atual nas ACLs de todos os objetos na hierarquia abaixo do objeto de destino. Para objetos que foram convertidos para o modelo de herança atual, os bits herdados auto herdados do SE da \_ DACL \_ e da \_ \_ SACL \_ \_ são definidos no campo de controle do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) do objeto.

Quando você cria um novo descritor de segurança que reflete o modelo de herança atual, é necessário ter cuidado para não alterar a semântica do descritor de segurança. Assim, as ACEs allow e Deny nunca são movidas em relação uma à outra. Se esse movimento for necessário (por exemplo, para posicionar todas as ACEs não herdadas na frente de uma ACL), a ACL será marcada como protegida para evitar a alteração semântica.

O sistema usa as seguintes regras ao propagar ACEs herdadas para objetos filho:

-   Se um objeto filho sem nenhuma DACL herdar uma ACE, o resultado será um objeto filho com uma DACL que contém apenas a ACE herdada.
-   Se um objeto filho com uma DACL vazia herdar uma ACE, o resultado será um objeto filho com uma DACL que contém apenas a ACE herdada.
-   Se você remover uma ACE herdável de um objeto pai, a herança automática removerá todas as cópias da ACE que foram herdadas por objetos filho.
-   Se a herança automática resultar na remoção de todas as ACEs da DACL de um objeto filho, o objeto filho terá uma DACL vazia em vez de nenhuma DACL.

Essas regras podem ter o resultado inesperado de converter um objeto sem DACL para um objeto com uma DACL vazia. Um objeto sem nenhuma DACL permite acesso completo, mas um objeto com uma DACL vazia não permite acesso. Como um exemplo de como essas regras podem criar uma DACL vazia, suponha que você adicione uma ACE herdável ao objeto raiz de uma árvore de objetos. A herança automática propaga a ACE herdável para todos os objetos na árvore. Os objetos filho que começaram com nenhuma DACL agora têm uma DACL com a ACE herdada. Se você remover a ACE herdável do objeto raiz, o sistema propagará automaticamente a alteração para os objetos filho. Os objetos filho iniciados sem nenhuma DACL (permitindo acesso completo) agora têm uma DACL vazia (não permitindo acesso).

Para garantir que um objeto filho sem nenhuma DACL não seja afetado por ACEs herdáveis, defina o \_ sinalizador se \_ protegido por DACL no descritor de segurança do objeto.

Para obter informações sobre como criar uma DACL corretamente, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
