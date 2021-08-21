---
title: Cancelando chamadas de método
description: Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar muito tempo para retornar.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ea089f257527dfd31d7120170c8749a2d1b4d60ba006843c7ff5d43403b352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311080"
---
# <a name="canceling-method-calls"></a>Cancelando chamadas de método

Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar muito tempo para retornar. A latência da conexão de rede pode ser alta, o computador do servidor pode estar atendendo a muitos clientes ou o componente do servidor pode estar passando uma grande quantidade de dados, como um arquivo multimídia. Os usuários devem ser capazes de cancelar uma solicitação que está demorando muito e o aplicativo deve ser capaz de lidar com solicitações de cancelamento e continuar com seu outro trabalho. No COM, você pode usar a interface [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar uma chamada pendente originada de um apartment de thread único.

Quando uma chamada é marshaled, o proxy cria um objeto cancel, que implementa a interface [**ICancelMethodCalls.**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) O objeto cancel está associado à chamada e ao thread no qual a chamada está pendente.

Para cancelar a chamada pendente, o cliente passa uma solicitação de cancelamento por meio do objeto cancel, que trata os detalhes de notificação do objeto de servidor de que a chamada foi cancelada. Se o método chamado não tiver retornado, o objeto de servidor, ao detectar a solicitação de cancelamento, limpará todos os recursos do programa alocados e notifica seu cliente, retornando um valor **HRESULT** apropriado, que ele cancelou a execução da chamada. Se o método chamado já tiver retornado, o objeto cancel notifica o cliente. Em ambos os casos, o thread do cliente é desbloqueado e pode continuar o processamento.

Como o objeto de servidor responde a uma solicitação de cancelamento está a critério do implementador do servidor, mas o thread de chamada no cliente sempre será desbloqueado e ignorará os resultados que o servidor tentar passar para ele. Os objetos Cancel fornecem um meio para solicitar que um método em execução no momento seja cancelado, mas não há nenhuma garantia de que o objeto de servidor interromperá o processamento da chamada. Por exemplo, a chamada pode já ter retornado ou o objeto de servidor pode não dar suporte a objetos de cancelamento.

O COM fornece automaticamente uma implementação padrão de objetos de cancelamento para objetos de cliente e interfaces que usam marshaling padrão. Para objetos e interfaces que usam marshaling personalizado, você precisará implementar seu próprio objeto de cancelamento.

Neste momento, os objetos de cancelamento lidam apenas com chamadas síncronas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Cancelando uma chamada assíncrona](canceling-an-asynchronous-call.md)
</dt> <dt>

[**CoGetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcancelobject)
</dt> <dt>

[**CoSetCancelObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetcancelobject)
</dt> <dt>

[**CoTestCancel**](/windows/desktop/api/combaseapi/nf-combaseapi-cotestcancel)
</dt> </dl>

 

 