---
description: Quando um processo tenta acessar um objeto de segurança, o sistema passa pelas ACEs (entradas de controle de acesso) na DACL (lista de controle de acesso discricionário) de objetos até encontrar ACEs que permitem ou negam o acesso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordem de ACEs em um DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b5d017fe6441e90cded6458d8796dee301e3fa0fda01b7d088039abd9834ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907746"
---
# <a name="order-of-aces-in-a-dacl"></a>Ordem de ACEs em um DACL

Quando [](/windows/desktop/SecGloss/p-gly) um processo tenta acessar um objeto de segurança, o sistema passa pelas ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) na DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) do objeto até encontrar ACEs que permitem ou negam o acesso solicitado. Os direitos de acesso que uma DACL permite a um usuário podem variar dependendo da ordem de ACEs na DACL. Consequentemente, Windows sistema operacional XP define uma ordem preferencial para ACEs na DACL de um objeto que pode ser proteger. A ordem preferencial fornece uma estrutura simples que garante que uma ACE negada pelo acesso realmente nega acesso. Para obter mais informações sobre o algoritmo do sistema para verificar o acesso, consulte [Como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).

Para Windows Server 2003 e Windows XP, a ordem adequada de ACEs é complicada pela introdução de ACEs específicas ao objeto e herança automática.

As etapas a seguir descrevem a ordem preferencial:

1.  Todas as ACEs explícitas são colocadas em um grupo antes de qualquer ACEs herdada.
2.  Dentro do grupo de ACEs explícitas, as ACEs de acesso negado são colocadas antes das ACEs permitidas para acesso.
3.  As ACEs herdadas são colocadas na ordem em que são herdadas. OS ACEs herdados do pai do objeto filho vêm primeiro, depois os ACEs herdados do descendente e assim por diante na árvore de objetos.
4.  Para cada nível de ACEs herdadas, as ACEs de acesso negado são colocadas antes das ACEs permitidas para acesso.

É claro que nem todos os tipos ACE são necessários em uma ACL.

Funções como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) adicionam uma ACE ao final de uma ACL. É responsabilidade do chamador garantir que as ACEs sejam adicionadas na ordem adequada.

 

 
