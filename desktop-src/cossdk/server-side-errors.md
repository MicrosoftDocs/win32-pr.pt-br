---
description: Erros de Server-Side
ms.assetid: ce8ddb52-237c-4d46-a088-9f592afadcd2
title: Erros de Server-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7946b8197553874b8da22d35f8fab5b83f14862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791059"
---
# <a name="server-side-errors"></a>Erros de Server-Side

O ouvinte e o Player trabalham juntos para lidar com mensagens suspeitas. Se uma transação que está sendo reproduzida falhar, o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) moverá a mensagem de entrada de volta para a fila de entrada. O Player anulará a transação se receber um HRESULT com falha do componente de servidor ou se ele detectar uma exceção. Se o problema persistir, o ouvinte poderá fazer um loop continuamente no seguinte padrão:

-   Remover a mensagem da fila
-   Instancia o objeto
-   Sofre uma reversão
-   Coloca a mensagem de volta na parte superior da fila

O serviço de componentes na fila trata dessa falha usando uma série de filas de repetição específicas do aplicativo. Criado quando o componente é instalado, há sete filas para cada aplicativo, da seguinte maneira:

1.  A fila de entrada normal. O nome dessa fila é o nome do aplicativo COM+. Esta é uma fila pública do enfileiramento de mensagens.

2.  A primeira fila de repetição. As mensagens serão movidas aqui se a transação falhar repetidamente ao processar mensagens da fila de entrada normal. As mensagens nessa fila são processadas após um minuto. Uma mensagem pode ser repetida três vezes nessa fila antes de ser movida para trás da segunda fila de repetição. Essa fila é denominada *ApplicationName* \_ 0. Essa fila é uma fila de enfileiramento de mensagens particular.

3.  A segunda fila de repetição. As mensagens serão movidas aqui se a transação falhar repetidamente ao processar mensagens da primeira fila de repetição. As mensagens nessa fila são processadas após dois minutos. Uma mensagem pode ser repetida três vezes nessa fila antes de ser movida para trás da terceira fila de repetição. Essa fila é denominada *ApplicationName* \_ 1. Essa fila é uma fila de enfileiramento de mensagens particular.

4.  A terceira fila de repetição. As mensagens serão movidas aqui se a transação falhar repetidamente ao processar mensagens da segunda fila de repetição. As mensagens nessa fila são processadas após quatro minutos. Uma mensagem pode ser repetida três vezes nessa fila antes de ser movida para trás da quarta fila de repetição. Essa fila é denominada *ApplicationName* \_ 2. Essa fila é uma fila de enfileiramento de mensagens particular.

5.  A quarta fila de repetição. As mensagens serão movidas aqui se a transação falhar repetidamente ao processar mensagens da terceira fila de repetição. As mensagens nessa fila são processadas após oito minutos. Uma mensagem pode ser repetida três vezes nessa fila antes de ser movida para a quinta fila de repetição. Essa fila é denominada *ApplicationName* \_ 3. Essa fila é uma fila de enfileiramento de mensagens particular.

6.  A quinta fila de repetição. As mensagens serão movidas aqui se a transação falhar repetidamente ao processar mensagens da quarta fila de repetição. As mensagens nessa fila são processadas após dezesseis minutos. Uma mensagem pode ser repetida três vezes nessa fila antes de ser movida para a fila de repouso final. Essa fila é denominada *ApplicationName* \_ 4. Esta é uma fila de enfileiramento de mensagens particular.

7.  Uma fila de repouso final específica do aplicativo. As mensagens serão movidas aqui se a transação for anulada repetidamente quando for tentada na quinta fila de repetição. Essa fila é denominada *ApplicationName* \_ DeadQueue. Esta é uma fila de enfileiramento de mensagens particular. A fila de repouso final não é atendida por um ouvinte de fila. As mensagens permanecem aqui até serem movidas manualmente (talvez pelo utilitário enfileiramento de mensagens dos componentes enfileirados) ou são limpas pelo Gerenciador de filas de mensagens.

Mensagens que não são reproduzidas porque estão claras de que todas as tentativas de repetição falham podem ser movidas diretamente para a fila de repouso final específica do aplicativo sem serem avançadas por todos os níveis de repetição.

O jogador emite um evento COM+ para notificar as partes interessadas de que as mensagens não podem ser reproduzidas. Os eventos COM+ são emitidos nas seguintes situações:

-   Quando uma transação é anulada
-   Quando uma mensagem é movida de uma fila para outra
-   Quando uma mensagem é depositada na fila de repouso final

As mensagens podem ser modificadas antes de passar de uma fila para outra. O mecanismo de segurança de componentes na fila COM+ permite que uma mensagem seja movida para as filas de repetição e, em seguida, reinserida na fila de entrada inicial do aplicativo. Para obter mais informações sobre segurança de componentes na fila, consulte [segurança de componentes na fila](queued-components-security.md).

As filas de repetição são criadas junto com a fila do aplicativo principal quando o aplicativo é marcado como enfileirado pela ferramenta de administração dos serviços de componentes ou usando as funções do SDK administrativo do COM+. O serviço de componentes na fila permite flexibilidade no mecanismo de repetição, permitindo que as filas de repetição sejam excluídas. Por exemplo, se todas as filas de repetição forem excluídas, uma mensagem que é anulada persistentemente será movida diretamente da fila de aplicativos para a fila de repouso final específica do aplicativo. Ao remover uma ou mais das filas de repetição, o número e o comprimento das repetições podem ser reduzidos. Se as filas forem removidas da sequência de repetição, o tempo das filas restantes corresponderá à posição na sequência de filas de repetição. Por exemplo, se você remover a fila de repetição *ApplicationName* \_ 1, *ApplicationName* \_ 2 e *ApplicationName* \_ 3, as mensagens no *ApplicationName* \_ 4 seriam processadas como se a fila fosse a segunda fila de repetição.

O mecanismo de repetição é projetado para concluir uma mensagem, se possível. Em alguns casos, pode não ser possível que a mensagem tenha sucesso. Por exemplo, um cliente pode estar tentando retirar dinheiro de uma conta que tenha fundos insuficientes. Nessas circunstâncias, você pode manipular o erro de várias maneiras, incluindo o seguinte:

-   Gerar um diagnóstico e emitir um aviso
-   Criar uma transação de compensação
-   Ignorar o problema e ignorar a mensagem

Como falhas persistentes do lado do cliente, o serviço de componentes em fila permite que uma classe de exceção seja associada a um componente. A classe de exceção é associada ao componente usando a guia **avançado** na página Propriedades do componente da ferramenta de administração de serviços de componentes ou usando as funções administrativas do com+. A classe de exceção permite que o desenvolvedor tenha controle depois que uma mensagem for repetida e antes que essa mensagem seja movida para a fila de repouso final específica do aplicativo. Para obter mais informações sobre a classe de exceção, consulte [falhas persistentes de Client-Side](persistent-client-side-failures.md).

A seguir está a sequência de eventos para a manipulação de exceção do lado do servidor:

1.  A mensagem é movida pelas filas de repetição específicas do aplicativo disponíveis.
2.  A repetição final da última fila de repetição falha.
3.  O tempo de execução do serviço de componentes na fila recupera o componente de destino da mensagem e verifica se há uma classe de exceção.
4.  O tempo de execução instancia a classe de exceção.
5.  As consultas de tempo de execução [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) na classe de exceção.
6.  O tempo de execução chama [**IPlaybackControl:: FinalServerRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalserverretry) na classe de exceção.
7.  O tempo de execução reproduz todas as chamadas de propriedade e método da mensagem para a classe de exceção.
8.  Se as etapas 4 a 6 não tiverem sucesso, o tempo de execução moverá a mensagem para a fila de repouso final específica do aplicativo.

Se você precisar intervir no processo descrito acima ou precisar mover uma mensagem suspeita para fora de sua fila de repouso final, use o utilitário de movimentação de mensagem. Para obter mais informações sobre o utilitário de movimentação de mensagens, consulte [tratamento de erros](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros do lado do cliente](client-side-errors.md)
</dt> <dt>

[Falhas de Client-Side persistentes](persistent-client-side-failures.md)
</dt> </dl>

 

 



