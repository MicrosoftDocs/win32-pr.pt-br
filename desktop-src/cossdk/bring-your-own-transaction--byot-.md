---
description: BYOT (Bring Your Own Transaction)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: BYOT (Bring Your Own Transaction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308659"
---
# <a name="bring-your-own-transaction-byot"></a>BYOT (Bring Your Own Transaction)

BYOT permite que um componente seja criado com ou herde uma transação externa. Ou seja, um componente que ainda não tem uma transação associada pode adquirir uma transação. Atualmente, as transações do MTS são automáticas; se uma instância de componente reside em uma transação é determinada no momento da criação. Os atributos transacionais de um componente e seu criador determinam qual transação está associada a uma determinada instância. Em todos os casos, o MTS controla os tempo de vida da transação. O COM+ estende isso para permitir a configuração de uma transação DTC ou TIP arbitrária pré-existente como a propriedade de transação do contexto de um novo componente. Isso permite que os componentes configurados sejam associados a transações cujos tempos de vida são controlados por um monitor TP, OTS ou DBMS.

> [!Note]  
> As transações BYOT devem ser usadas com cuidado. Em determinadas situações, elas podem resultar em uma transação que abrange vários domínios de sincronização, ou seja, permitem o paralelismo com uma transação, causando uma condição de deadlock. Transações automáticas, em vez de transações BYOT, são o modelo de programação preferencial para os autores de componentes de negócios.

 

As interfaces para transações BYOT incluem a interface [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e a interface [**ICreateWithTipTransactionEx.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) A interface **ICreateWithTransactionEx** cria um objeto que é inscrito em uma transação manual. A interface **ICreateWithTipTransactionEx** cria um objeto que é inscrito em uma transação manual usando o TIP (Transaction Internet Protocol).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Herdando transações manuais](inheriting-manual-transactions.md)
</dt> </dl>

 

 



