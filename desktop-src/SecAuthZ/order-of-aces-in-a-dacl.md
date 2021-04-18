---
description: Quando um processo tenta acessar um objeto protegível, o sistema percorre as ACEs (entradas de controle de acesso) na DACL (lista de controle de acesso discricional) dos objetos até encontrar as ACEs que permitem ou negam o acesso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Ordem das ACEs em uma DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769193"
---
# <a name="order-of-aces-in-a-dacl"></a>Ordem das ACEs em uma DACL

Quando um [*processo*](/windows/desktop/SecGloss/p-gly) tenta acessar um objeto protegível, o sistema percorre as ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) do objeto até encontrar ACEs que permitam ou negue o acesso solicitado. Os direitos de acesso que uma DACL permite que um usuário variem dependendo da ordem das ACEs na DACL. Consequentemente, o sistema operacional Windows XP define uma ordem preferida para ACEs na DACL de um objeto protegível. A ordem preferida fornece uma estrutura simples que garante que uma ACE de acesso negado realmente negue acesso. Para obter mais informações sobre o algoritmo do sistema para verificar o acesso, consulte [como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md).

Para o Windows Server 2003 e o Windows XP, a ordem correta das ACEs é complicada pela introdução de ACEs específicas de objeto e herança automática.

As etapas a seguir descrevem a ordem preferida:

1.  Todas as ACEs explícitas são colocadas em um grupo antes de quaisquer ACEs herdadas.
2.  Dentro do grupo de ACEs explícitas, ACEs com acesso negado são colocadas antes das ACEs permitidas pelo Access.
3.  As ACEs herdadas são colocadas na ordem em que são herdadas. As ACEs herdadas do pai do objeto filho aparecem primeiro, então as ACEs herdadas do avô e assim por diante na árvore de objetos.
4.  Para cada nível de ACEs herdadas, as ACEs de acesso negado são colocadas antes das ACEs permitidas pelo Access.

É claro que nem todos os tipos de ACE são necessários em uma ACL.

Funções como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) e [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) adicionam uma ACE ao final de uma ACL. É responsabilidade do chamador garantir que as ACEs sejam adicionadas na ordem correta.

 

 
