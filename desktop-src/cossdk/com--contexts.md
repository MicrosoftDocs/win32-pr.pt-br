---
description: Para componentes configurados em execução em aplicativos COM+, os contextos são a base na qual os serviços COM+ são fornecidos.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contextos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c48e2fb9a118bff5fe4d6590ff859f0f053ab29687d4f4a2a070d44af37b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730646"
---
# <a name="com-contexts"></a>Contextos COM+

Para componentes configurados em execução em aplicativos COM+, *os contextos* são a base na qual os serviços COM+ são fornecidos. No COM+, um contexto é definido como conjunto de propriedades de tempo de executar associadas a um ou mais objetos COM usados para fornecer serviços para esses objetos.

No COM+, cada objeto COM é associado com precisamente um contexto à medida que é executado (ou seja, entre sua ativação e desativação) e cada contexto reside exatamente em um apartment COM. Vários objetos podem ser executados no mesmo contexto e vários contextos podem residir no mesmo apartment. Inicializadas quando um objeto é ativado, as propriedades de contexto, como propriedades de contexto de segurança, representam as necessidades de tempo de executar de um objeto.

> [!Note]  
> Para componentes não configurados que não usam serviços COM+, o contexto é, na maior parte, ignorado.

 

O COM+ usa propriedades de contexto como base para fornecer serviços em tempo de executar. Essas propriedades têm o estado que determina como o ambiente de execução executa serviços para objetos dentro do contexto. Em alguns casos, você pode interagir diretamente com as propriedades de contexto de um objeto para indicar algum estado relevante para um serviço que está sendo fornecido para o objeto. Por exemplo, você faria isso quando um objeto que participasse de uma transação automática votasse no resultado da transação.

Para ver uma discussão detalhada sobre a base COM desses conceitos, consulte [Processos, threads e apartments.](/windows/desktop/com/processes--threads--and-apartments)

## <a name="programmatic-interaction-with-context-properties"></a>Interação programática com propriedades de contexto

Cada contexto tem um objeto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) associado que mantém o controle de suas propriedades. Você pode acessar **ObjectContext** chamando a [**função GetObjectContext.**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) Depois de acessar **ObjectContext**, você pode chamar métodos na interface [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) que ela expõe para manipular propriedades de contexto.

Por exemplo, chamar [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) tem o efeito de definir o bit de consistência da transação como "consistente" e o bit de ativação [JIT](com--just-in-time-activation.md) feito como "done" no contexto associado ao objeto. "Consistente" sinaliza para COM+ que você vota para fazer commit da transação e "done" indica que o objeto está pronto para ser desativado quando o método retorna.

Além de [**IObjectContext,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)outras interfaces especializadas que fornece acesso às propriedades de contexto são [**IObjectContextInfo,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo) [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)e [**IObjectContextActivity.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity) Até certo ponto, [**ISecurityCallContext também**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) acessa propriedades de contexto. Você pode usar [**IGetSecurityCallContext::GetSecurityCallContext para**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) obter **ISecurityCallContext.**

## <a name="understanding-activation-and-interception"></a>Noções básicas sobre ativação e interceptação

Em geral, você precisa pensar no contexto apenas na medida em que ele representa várias propriedades, algumas das quais você pode definir ou obter, que são usadas para fornecer serviços COM+ para seus componentes. Em algumas circunstâncias, no entanto, talvez seja necessário considerar as duas facetas inter-relacionadas a seguir de contextos com mais detalhes:

-   [Ativação de](context-activation.md)contexto ou a inicialização de um objeto em um contexto apropriado.
-   [Interceptação](interception-of-cross-context-calls.md)ou o que o COM+ faz em chamadas em um limite de contexto.

## <a name="relation-to-mts-context-wrappers"></a>Relação com wrappers de contexto do MTS

Os contextos substituem efetivamente os wrappers de contexto do MTS. A finalidade que eles serviram – fornecer serviços automáticos interceptando solicitações de criação – agora é um recurso integrado do COM+. Como resultado, você não precisa mais usar a [**função SafeRef.**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) No MTS, **SafeRef** foi usado para obter uma referência ao objeto que pode ser passada fora do wrapper de contexto. No COM+, isso é desnecessário; as referências de objeto normal **(este** ponteiro) funcionam.

 

 
