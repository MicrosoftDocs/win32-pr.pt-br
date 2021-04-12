---
description: No modelo de programação COM+, você pode criar seus componentes para fazer o que eles fazem melhor&\# 8212; habilitar a lógica de negócios ou estabelecer uma conexão de banco de dados&\# 8212; e contar com a estrutura de processamento de transações do Microsoft Windows para automatizar transações.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gerenciando transações automáticas no COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501051"
---
# <a name="managing-automatic-transactions-in-com"></a>Gerenciando transações automáticas no COM+

No modelo de programação COM+, você pode projetar seus componentes para fazer o que eles fazem melhor — habilitar a lógica de negócios ou estabelecer uma conexão de banco de dados — e contar com a estrutura de processamento de transações do Microsoft Windows para automatizar transações.

## <a name="starting-a-transaction"></a>Iniciando uma transação

O COM+ inicia automaticamente uma transação quando encontra uma das seguintes condições:

-   Quando um cliente não transacional chama um componente que requer uma transação ou requer uma nova transação.
-   Quando um cliente transacional chama um componente que requer uma nova transação.

Se o COM+ determinar que um objeto deve ter uma nova transação, ele iniciará a transação primeiro e, em seguida, colocará o objeto nela. O processo inclui as seguintes etapas:

1.  O COM+ cria um objeto de contexto, define os atributos de [ativação JIT](com--just-in-time-activation.md) e de [sincronização](com--synchronization.md) como Required e define os [sinalizadores consistentes e concluídos](consistent-and-done-flags.md) como true e false, respectivamente.
2.  O COM+ se comunica com o Coordenador de Transações Distribuídas (DTC) para iniciar uma transação. O DTC coordena a transação física.
3.  O DTC gera um identificador de transação e o passa de volta para o COM+. O identificador de transação estabelece um limite de transação. Todos os objetos que participam da transação compartilham o mesmo identificador.
4.  Quando o cliente cria o objeto, o COM+ o ativa dentro do limite da transação.

## <a name="ending-a-transaction"></a>Finalizando uma transação

O COM+ encerra uma transação automática confirmando ou anulando-a quando uma das seguintes condições ocorre:

-   O objeto raiz da transação conclui seu trabalho e o COM+ o libera. Depois que o objeto raiz é desativado, a transação tenta confirmar.
-   O cliente libera o objeto raiz. Sem uma referência, o objeto raiz é desativado e a transação tenta confirmar.
-   A transação excede o limite de tempo limite. A transação é anulada automaticamente se não confirmada no período de tempo limite da transação, desativando todos os objetos associados à transação. O período de tempo limite de transação padrão é de 60 segundos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sinalizadores consistentes e concluídos](consistent-and-done-flags.md)
</dt> <dt>

[Acelerando as transações notificando o objeto raiz](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[Finalizando uma transação automática chamando SetComplete](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 



