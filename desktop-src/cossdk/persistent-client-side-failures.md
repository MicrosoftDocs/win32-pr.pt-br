---
description: Falhas de Client-Side persistentes
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Falhas de Client-Side persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d303e712257d62e4ae42497cb4463e782cfbb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370444"
---
# <a name="persistent-client-side-failures"></a>Falhas de Client-Side persistentes

Em alguns casos, o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pode mover uma mensagem para a fila de destino. Por exemplo, se os controles de acesso à fila não permitirem que a mensagem seja movida do cliente para o servidor, a mensagem incorreta será movida para a fila de mensagens mortas do lado do cliente. Quando isso ocorre, o serviço de componentes em fila do COM+ permite que uma classe de exceção seja associada a um componente. Para associar a classe de exceção ao componente, use a guia **avançado** na página Propriedades do componente da ferramenta de administração de serviços de componentes. Você também pode associar a classe de exceção programaticamente, usando o atributo de componente de catálogo ExceptionClass das funções administrativas do COM+.

A classe de exceção é definida como o ProgID ou o CLSID de um componente que implementa [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). O serviço de componentes em fila tem um monitor de fila de mensagens mortas que verifica a fila de mensagens mortas de transação. Se houver uma mensagem na fila, o monitor da fila de mensagens mortas criará uma instância do manipulador de exceção associado ao componente de destino e chamará [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), indicando que houve um erro irrecuperável no lado do cliente.

Além de [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), o manipulador de exceção deve implementar o mesmo conjunto de interfaces que o componente de servidor para o qual está tratando exceções. Quando [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) é chamado, o tempo de execução dos componentes em fila reproduz a mensagem com falha para o manipulador de exceção. Isso permite que o manipulador de exceção implemente um comportamento alternativo para mensagens que não podem ser movidas para o servidor — por exemplo, gerando uma transação de compensação.

Se o manipulador de exceção concluir todas as chamadas de método reproduzidas, a mensagem será removida da fila de mensagens mortas de transação e será ignorada. No entanto, se o manipulador de exceção abortar a mensagem retornando um status de falha de uma das chamadas de método, a mensagem será retornada para a fila de mensagens mortas de transação. A sequência de eventos a seguir mostra como as exceções do lado do cliente são tratadas:

1.  O serviço de enfileiramento de mensagens não entrega uma mensagem ao servidor e coloca a mensagem na fila de mensagens mortas da transação.
2.  O ouvinte da fila de mensagens mortas (DLQL) localiza uma mensagem na fila de mensagens mortas do transação.
3.  O DLQL recupera o CLSID do componente de destino da mensagem e verifica se há uma classe de exceção.
4.  O DLQL instancia a classe de exceção.
5.  O DLQL consulta [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) para a classe de exceção.
6.  O DLQL chama o método [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) na classe de exceção.
7.  O DLQL reproduz todas as chamadas de propriedade e método da mensagem para a classe de exceção.
8.  O DLQL excluirá a mensagem se o manipulador de exceção concluir a transação com êxito. O manipulador de exceção pode emitir [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)e a mensagem permanecerá na fila de mensagens mortas.

Se qualquer uma das etapas anteriores falhar, a mensagem será deixada na fila de mensagens mortas da transação.

Quando iniciado, o DLQL lê cada mensagem na fila de mensagens mortas transacionais de enfileiramento de mensagem e instancia a classe de exceção para cada mensagem de componentes na fila. Depois de uma passagem pela fila, ela aguarda novas mensagens. Em seguida, ele processa cada nova mensagem de fila de mensagens mortas à medida que chega.

Se você precisar intervir no processo descrito aqui ou se precisar mover uma mensagem suspeita para fora de sua fila de repouso final, use o utilitário de movimentação de mensagem. Para obter mais informações sobre o utilitário de movimentação de mensagens, consulte [tratamento de erros](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros do lado do cliente](client-side-errors.md)
</dt> <dt>

[Erros do lado do servidor](server-side-errors.md)
</dt> </dl>

 

 



