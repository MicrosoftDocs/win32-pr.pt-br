---
description: Traga sua própria transação (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Traga sua própria transação (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764595"
---
# <a name="bring-your-own-transaction-byot"></a>Traga sua própria transação (BYOT)

O BYOT permite que um componente seja criado com ou para herdar uma transação externa. Ou seja, um componente que ainda não tem uma transação associada pode adquirir uma transação. Atualmente, as transações MTS são automáticas; se uma instância de componente reside em uma transação é determinada no momento da criação. Os atributos transacionais de um componente e seu criador determinam qual transação está associada a uma determinada instância. Em todos os casos, o MTS controla os tempos de vida das transações. O COM+ estende isso para permitir a definição de uma transação do DTC ou TIP preexistente arbitrária como a propriedade Transaction do contexto de um novo componente. Isso permite que os componentes configurados sejam associados a transações cujos tempos de vida são controlados por um monitor TP, OTS ou DBMS.

> [!Note]  
> As transações de BYOT devem ser usadas com cautela. Em determinadas situações, eles podem resultar em uma transação que abrange vários domínios de sincronização, ou seja, eles permitem paralelismo com uma transação, causando uma condição de deadlock. Transações automáticas, em vez de transações de BYOT, são o modelo de programação preferencial para escritores de componentes comerciais.

 

As interfaces para transações de BYOT incluem a interface [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e a interface [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) . A interface **ICreateWithTransactionEx** cria um objeto que é inscrito em uma transação manual. A interface **ICreateWithTipTransactionEx** cria um objeto que é inscrito em uma transação manual usando o TIP (protocolo de Internet de transação).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Herdando transações manuais](inheriting-manual-transactions.md)
</dt> </dl>

 

 



