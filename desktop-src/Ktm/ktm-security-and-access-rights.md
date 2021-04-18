---
description: O modelo de segurança do Windows permite que chamadores de KTM (kernel Transaction Manager) controlem o acesso a transações, Gerenciador de transações, Gerenciador de recursos e objetos de inscrição.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Segurança de KTM e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767783"
---
# <a name="ktm-security-and-access-rights"></a>Segurança de KTM e direitos de acesso

O modelo de segurança do Windows permite que chamadores de KTM (kernel Transaction Manager) controlem o acesso a transações, Gerenciador de transações, Gerenciador de recursos e objetos de inscrição. Para obter mais informações, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model). Para aplicativos que não se preocupam com a segurança, as transações podem ser criadas com ACLs (listas de controle de acesso) permissivas que permitem que qualquer Gerenciador de recursos se inscreva em uma transação.

## <a name="transactions"></a>Transactions

Quando um cliente usa a função [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança do objeto de transação.

Os direitos de acesso válidos para objetos de transação incluem a capacidade de consultar e definir informações, inscrever-se e várias operações de transação, bem como [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). As [**máscaras de acesso à transação**](transaction-access-masks.md) listam os direitos de acesso específicos para uma transação.

Como as transações têm um estado durável, é essencial que o RMs e TMs que interagem com o KTM atendam às suas obrigações em relação à recuperação. A falha em atender a essas obrigações pode resultar em vazamentos de recursos que não são limpos, mesmo por uma reinicialização do sistema. Considere o efeito de um vazamento persistente ou código mal-intencionado que fazia com que o KTM consumisse recursos de kernel até que ele resultasse em uma falha do sistema; após a reinicialização resultante, o KTM lerá seu log e recriaria todos os objetos persistentes, potencialmente causando a recorrência da mesma falha do sistema. A limitação baseada em cota impedirá a privação de recursos persistentes de um RM invasor ou mal comportado. Por fim, os mecanismos administrativos devem ser criados para permitir a detecção e a correção de vazamentos persistentes.

## <a name="transaction-managers"></a>Gerenciadores de transações

Quando um cliente usa a função [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança do objeto do Resource Manager.

Os direitos de acesso válidos para objetos do Gerenciador de transações incluem a capacidade de consultar e definir informações, criar RMs e recuperar e renomear operações, bem como [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). As [**máscaras de acesso do Gerenciador de transações**](transaction-manager-access-masks.md) listam os direitos de acesso específicos para um Gerenciador de transações.

Um Gerenciador de recursos pode criar seus próprios objetos do Gerenciador de transações com ACLs restritivas para limitar quais gerenciadores de recursos podem participar de transações que usam o log do Gerenciador de transações.

## <a name="resource-managers"></a>Gerenciadores de recursos

Quando um cliente usa a função [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança do objeto do Resource Manager.

Os direitos de acesso válidos para objetos do Resource Manager incluem a capacidade de consultar e definir informações, recuperar, inscrever, operações de registro, operações de propagação e recuperação, bem como [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). As [**máscaras de acesso do Gerenciador de recursos**](resource-manager-access-masks.md) listam os direitos de acesso específicos para um Gerenciador de recursos.

Um Gerenciador de recursos pode criar seus próprios objetos do Resource Manager com ACLs restritivas se quiser impedir que um código mal-intencionado intercepte notificações ou Force resultados transacionais específicos.

## <a name="enlistments"></a>Inscrições

Quando um cliente usa a função [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança para o objeto de inscrição.

Os direitos de acesso válidos para objetos de inscrição incluem a capacidade de consultar e definir informações, recuperar operações, bem como [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). As [**máscaras de acesso à inscrição**](enlistment-access-masks.md) listam os direitos de acesso específicos para uma inscrição.

 

 
