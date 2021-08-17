---
description: Erros de Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Erros de Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c27c73cd2be39d98c881021e1a042f15dc623766af0d52a578c6cd49c30e0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129358"
---
# <a name="client-side-errors"></a>Erros de Client-Side

As falhas do lado do cliente são tratadas de forma semelhante às falhas do lado do servidor. O [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) pode mover uma mensagem para sua fila de destino se, por exemplo, a mensagem não puder ser movida do cliente para o servidor. Nesse caso, a mensagem é movida para a fila de mensagens mortas do lado do cliente.

O serviço de componentes em fila COM+ monitora a fila de mensagens mortas. Se as mensagens tiverem sido movidas, o serviço de componentes em fila criará uma instância da classe de exceção e chamará [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol). Se isso for bem-sucedido, o monitor da fila de mensagens mortas invocará [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry).

O objeto pode tomar alguma atitude para reverter o efeito de uma transação anterior. Se a reprodução for confirmada, a mensagem será removida da fila de mensagens mortas da transação. Se a reprodução falhar ou se o CLSID e a interface necessários não estiverem disponíveis, a mensagem permanecerá na fila de mensagens mortas do transação.

Se você precisar intervir no processo descrito acima ou se precisar mover uma mensagem suspeita para fora de sua fila de repouso final, use o utilitário de movimentação de mensagem. Para obter mais informações sobre o utilitário de movimentação de mensagens, consulte [tratamento de erros](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Falhas de Client-Side persistentes](persistent-client-side-failures.md)
</dt> <dt>

[Erros do lado do servidor](server-side-errors.md)
</dt> </dl>

 

 
