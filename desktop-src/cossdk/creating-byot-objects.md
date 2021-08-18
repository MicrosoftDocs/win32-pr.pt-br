---
description: Criando objetos BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Criando objetos BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128758"
---
# <a name="creating-byot-objects"></a>Criando objetos BYOT

Um novo objeto BYOT cria objetos com transações manuais. As duas interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), têm um único método, **CreateInstance**, que assumem um ponteiro de interface **ITransaction** e uma URL Tip, respectivamente. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) retorna um ponteiro de interface para o objeto recém-criado, que é inscrito na transação especificada.

Quando um objeto com uma transação manual é liberado, o COM+ não tenta confirmar a transação. A transação é controlada explicitamente pelo Gerenciador de transações externas que dispensava a transação sob a qual esse objeto foi criado.

> [!Note]  
> O objeto BYOT. ByotServerEx precisa ser importado para um aplicativo COM+.

 

 

 



