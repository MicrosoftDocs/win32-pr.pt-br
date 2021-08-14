---
description: O Windows de segurança permite que os chamadores do KTM (Kernel Transaction Manager) controlem o acesso a transações, gerenciador de transações, gerenciador de recursos e objetos de inserção.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Direitos de acesso e segurança KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0baf273b45a886e40c731c44c261f836fdc0b79012f906a1b4adfe07083be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388885"
---
# <a name="ktm-security-and-access-rights"></a>Direitos de acesso e segurança KTM

O Windows de segurança permite que os chamadores do KTM (Kernel Transaction Manager) controlem o acesso a transações, gerenciador de transações, gerenciador de recursos e objetos de inserção. Para obter mais informações, consulte [Modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model). Para aplicativos que não estão preocupados com a segurança, as transações podem ser criadas com ACLs (listas de controle de acesso) permissivas que permitem que qualquer gerenciador de recursos se insliste em uma transação.

## <a name="transactions"></a>Transactions

Quando um cliente usa a [**função OpenTransaction,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança para o objeto de transação.

Os direitos de acesso válidos para objetos de transação incluem a capacidade de consultar e definir informações, inscrever-se e várias operações de transação, bem como [direitos de acesso padrão.](/windows/desktop/SecAuthZ/standard-access-rights) [**As Máscaras de Acesso à Transação**](transaction-access-masks.md) listam os direitos de acesso específicos para uma transação.

Como as transações têm um estado durável, é essencial que as RMs e as TMs que interagem com a KTM cumpram suas obrigações em relação à recuperação. A falha ao cumprir essas obrigações pode resultar em vazamentos de recursos que não são limpos, mesmo por uma reinicialização do sistema. Considere o efeito de um vazamento persistente ou código mal-intencionado que fez com que o KTM consumisse recursos de kernel até que resultasse em uma falha do sistema; após a reinicialização resultante, o KTM leria seu log e criaria todos os objetos persistentes, potencialmente causando a mesma falha do sistema. A throttling baseada em cota impedirá a falta de recursos persistentes de um RM mal-comportado ou mal-comportado. Por fim, é necessário criar mecanismos administrativos que permitam a detecção e a correção desses vazamentos persistentes.

## <a name="transaction-managers"></a>Gerenciadores de Transações

Quando um cliente usa a [**função OpenTransactionManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança para o objeto do gerenciador de recursos.

Os direitos de acesso válidos para objetos do gerenciador de transações incluem a capacidade de consultar e definir informações, criar RMs e recuperar e renomear operações, bem como direitos [de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). [**As Máscaras de Acesso do Gerenciador de**](transaction-manager-access-masks.md) Transações listam os direitos de acesso específicos para um gerenciador de transações.

Um gerenciador de recursos pode criar seus próprios objetos do gerenciador de transações com ACLs restritivas para limitar quais gerenciadores de recursos podem participar de transações que usam o log desse gerenciador de transações.

## <a name="resource-managers"></a>Gerenciadores de Recursos

Quando um cliente usa a [**função OpenResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança para o objeto do gerenciador de recursos.

Os direitos de acesso válidos para objetos do Resource Manager incluem a capacidade de consultar e definir informações, recuperar, inscrever, operações de registro e propagar e recuperar operações, bem como direitos de [acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). [**Resource Manager Máscaras de Acesso**](resource-manager-access-masks.md) lista os direitos de acesso específicos para um gerenciador de recursos.

Um gerenciador de recursos pode criar seus próprios objetos do gerenciador de recursos com ACLs restritivas se quiser impedir que um código mal-intencionado intercepte notificações ou force resultados transacionais específicos.

## <a name="enlistments"></a>Inscrições

Quando um cliente usa a [**função OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança para o objeto de inscrição.

Os direitos de acesso válidos para objetos de inscrução incluem a capacidade de consultar e definir informações, operações de recuperação, bem como [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights). [**As Máscaras de Acesso à Inscrever-se**](enlistment-access-masks.md) listam os direitos de acesso específicos para uma insrução.

 

 
