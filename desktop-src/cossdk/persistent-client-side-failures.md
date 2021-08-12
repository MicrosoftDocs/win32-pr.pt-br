---
description: Falhas Client-Side persistentes
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Falhas Client-Side persistentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305769"
---
# <a name="persistent-client-side-failures"></a>Falhas Client-Side persistentes

Em alguns casos, [o Enfiling de](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Mensagens pode mover uma mensagem para a fila de destino. Por exemplo, se os controles de acesso à fila não permitirem que a mensagem seja movida do cliente para o servidor, a mensagem errada será movida para a fila de mensagens mortas do lado do cliente. Quando isso ocorre, o serviço de componentes em fila COM+ permite que uma classe de exceção seja associada a um componente. Para associar a classe de exceção ao componente, use a **guia Avançado** na página de propriedades do componente da ferramenta de administração dos Serviços de Componentes. Você também pode associar a classe de exceção programaticamente, usando o atributo de componente de catálogo ExceptionClass das funções administrativas COM+.

A classe de exceção é definida como ProgID ou CLSID de um componente que implementa [**IPlaybackControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) O serviço de componentes na fila tem um monitor de fila de letras mortas que examina a fila de letra morta do Xact. Se houver uma mensagem na fila, o monitor de fila de mensagens mortas instancie o manipulador de exceção associado ao componente de destino e chama [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry), indicando que houve um erro irrecuperável no lado do cliente.

Além de [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol), o manipulador de exceção deve implementar o mesmo conjunto de interfaces que o componente de servidor para o qual está tratando exceções. Quando [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) é chamado, o run-time dos componentes na fila reproduz a mensagem com falha para o manipulador de exceção. Isso permite que o manipulador de exceção implemente um comportamento alternativo para mensagens que não podem ser movidas para o servidor, por exemplo, gerando uma transação de compensação.

Se o manipulador de exceção concluir todas as chamadas de método tocadas, a mensagem será removida da fila de mensagens mortas do Xact e será descartada. No entanto, se o manipulador de exceção anular a mensagem retornando um status de falha de uma das chamadas de método, a mensagem será retornada para a fila de mensagens mortas do Xact. A seguinte sequência de eventos mostra como as exceções do lado do cliente são tratadas:

1.  O Enfiling de Mensagens falha ao entregar uma mensagem ao servidor e coloca a mensagem na fila de mensagens mortas do Xact.
2.  O DLQL (ouvinte de fila de mensagens mortas) localiza uma mensagem na fila de mensagens mortas do Xact.
3.  O DLQL recupera o CLSID do componente de destino da mensagem e verifica se há uma classe de exceção.
4.  O DLQL instalita a classe de exceção.
5.  As consultas DLQL para [**IPlaybackControl para**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) a classe de exceção.
6.  O DLQL chama o [**método IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) na classe de exceção.
7.  O DLQL reproduz todas as chamadas de propriedade e método da mensagem para a classe de exceção.
8.  O DLQL excluirá a mensagem se o manipulador de exceção concluir a transação com êxito. O manipulador de exceção [**pode emitir IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)e a mensagem permanecerá na fila de mensagens mortas.

Se qualquer uma das etapas anteriores falhar, a mensagem será deixada na fila de mensagens mortas do Xact.

Quando iniciado, o DLQL lê cada mensagem na fila de mensagens mortas transacionais do Enfilamento de Mensagens e instanciou a classe de exceção para cada mensagem de componentes na fila. Depois de passar pela fila, ele aguarda novas mensagens. Em seguida, ele processa cada nova mensagem da fila de mensagens mortas conforme ela chega.

Se você precisar intervir no processo descrito aqui ou se precisar mover uma mensagem falsa para fora da fila final, use o utilitário de movimentação de mensagens. Para obter mais informações sobre o utilitário de movimentação de mensagens, consulte [Tratamento de erros](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros do lado do cliente](client-side-errors.md)
</dt> <dt>

[Erros do lado do servidor](server-side-errors.md)
</dt> </dl>

 

 



