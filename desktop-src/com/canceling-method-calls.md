---
title: Cancelando chamadas de método
description: Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar um tempo muito demorado para retornar.
ms.assetid: 18228ff1-8c1c-430a-ae5f-0e9a56b0fe3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a78f042e528036135df4865e8a454cd687da
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105797997"
---
# <a name="canceling-method-calls"></a>Cancelando chamadas de método

Com a introdução de aplicativos distribuídos e baseados na Web, algumas chamadas de método podem levar um tempo muito demorado para retornar. A latência da conexão de rede pode ser alta, a máquina do servidor pode estar atendendo a vários clientes ou o componente do servidor pode estar passando uma grande quantidade de dados, como um arquivo de multimídia. Os usuários devem ser capazes de cancelar uma solicitação que está demorando muito e o aplicativo deve ser capaz de lidar com solicitações de cancelamento e continuar com seu outro trabalho. Em COM, você pode usar a interface [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) para cancelar uma chamada pendente originada de um apartamento single-threaded.

Quando uma chamada é empacotada, o proxy cria um objeto Cancel, que implementa a interface [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) . O objeto Cancel é associado à chamada e ao thread no qual a chamada está pendente.

Para cancelar a chamada pendente, o cliente passa uma solicitação de cancelamento por meio do objeto Cancel, que manipula os detalhes da notificação do objeto de servidor que a chamada foi cancelada. Se o método chamado não tiver retornado, o objeto Server, na detecção da solicitação de cancelamento, limpará os recursos do programa que ele alocou e notificará seu cliente, retornando um valor **HRESULT** apropriado, que ele cancelou a execução da chamada. Se o método chamado já tiver retornado, o objeto Cancel notificará o cliente. Em ambos os casos, o thread do cliente é desbloqueado e pode continuar o processamento.

A forma como o objeto de servidor responde a uma solicitação de cancelamento é a critério do implementador do servidor, mas o thread de chamada no cliente sempre será desbloqueado e ignorará quaisquer resultados que o servidor tentar passar para ele. Os objetos Cancel fornecem um meio de solicitar que um método em execução no momento seja cancelado, mas não há nenhuma garantia de que o objeto de servidor pare de processar a chamada. Por exemplo, a chamada pode já ter sido retornada ou o objeto de servidor pode não dar suporte a objetos Cancel.

O COM fornece automaticamente uma implementação padrão de objetos de cancelamento para objetos de cliente e interfaces que usam marshaling padrão. Para objetos e interfaces que usam marshaling personalizado, você precisará implementar seu próprio objeto Cancel.

Neste momento, o cancelamento de objetos lida apenas com chamadas síncronas.

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

 

 